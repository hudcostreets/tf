<template>
  <div v-if="enabled" class="autoplay-controls">
    <button class="play-pause" @click.stop="toggle" :title="paused ? 'Play (space)' : 'Pause (space)'">
      <svg class="ring" viewBox="0 0 40 40">
        <circle class="track" cx="20" cy="20" r="18" />
        <circle class="indicator" cx="20" cy="20" r="18" :style="{ strokeDashoffset: dashOffset }" />
      </svg>
      <span class="icon">{{ paused ? '▶' : '❚❚' }}</span>
    </button>
    <button class="duration" @click.stop="changeDuration" title="Click to set seconds per step">
      {{ delay }}s
    </button>
  </div>
</template>
<script setup lang="ts">
import { computed, onMounted, ref } from 'vue'
import { useNav } from '@slidev/client'

const nav = useNav()
const enabled = ref(false)
const paused = ref(false)
const delay = ref(4.5)
const progress = ref(0)
let timer: number | null = null
let raf: number | null = null
let cycleStart = 0

const RADIUS = 18
const CIRC = 2 * Math.PI * RADIUS
const dashOffset = computed(() => progress.value * CIRC)

function tick() {
  if (nav.currentSlideNo.value >= nav.total.value && !nav.hasNext.value) nav.go(1)
  else nav.next()
  cycleStart = performance.now()
  progress.value = 0
}

function animate(now: number) {
  if (paused.value) return
  const elapsed = (now - cycleStart) / 1000
  progress.value = Math.min(elapsed / delay.value, 1)
  raf = requestAnimationFrame(animate)
}

function start() {
  if (timer) clearInterval(timer)
  if (raf) cancelAnimationFrame(raf)
  paused.value = false
  cycleStart = performance.now()
  progress.value = 0
  timer = window.setInterval(tick, delay.value * 1000)
  raf = requestAnimationFrame(animate)
}

function stop() {
  if (timer) { clearInterval(timer); timer = null }
  if (raf) { cancelAnimationFrame(raf); raf = null }
  paused.value = true
}

function toggle() {
  if (!enabled.value) return
  if (paused.value) start()
  else stop()
}

function changeDuration() {
  if (!enabled.value) return
  const cur = delay.value.toString()
  const v = window.prompt('Seconds per step:', cur)
  if (v === null) return
  const n = parseFloat(v)
  if (!Number.isFinite(n) || n <= 0) return
  delay.value = n
  if (!paused.value) start()
}

function onKey(e: KeyboardEvent) {
  if (!enabled.value) return
  if (e.code === 'Space') {
    e.preventDefault()
    e.stopImmediatePropagation()
    toggle()
  }
}

onMounted(() => {
  const sec = parseFloat(new URLSearchParams(location.search).get('a') || '0')
  if (sec > 0) {
    delay.value = sec
    enabled.value = true
    window.addEventListener('keydown', onKey, true)
    start()
  }
})
</script>
<style scoped>
.autoplay-controls {
  position: fixed;
  top: 0.6rem;
  right: 0.6rem;
  z-index: 9999;
  display: flex;
  flex-direction: column;
  gap: 0.35rem;
  align-items: flex-end;
  font-family: monospace;
}
.play-pause {
  position: relative;
  width: 2.5rem;
  height: 2.5rem;
  padding: 0;
  border: none;
  background: rgba(0, 0, 0, 0.55);
  border-radius: 50%;
  cursor: pointer;
  opacity: 0.8;
}
.play-pause:hover { opacity: 1; }
.ring {
  position: absolute;
  inset: 0;
  width: 100%;
  height: 100%;
  transform: rotate(-90deg);
}
.track {
  fill: none;
  stroke: rgba(255, 255, 255, 0.15);
  stroke-width: 3;
}
.indicator {
  fill: none;
  stroke: white;
  stroke-width: 3;
  stroke-dasharray: 113.0973;
}
.icon {
  position: absolute;
  inset: 0;
  display: flex;
  align-items: center;
  justify-content: center;
  color: white;
  font-size: 0.85rem;
  pointer-events: none;
}
.duration {
  background: rgba(0, 0, 0, 0.55);
  border: 1px solid rgba(255, 255, 255, 0.35);
  border-radius: 4px;
  padding: 0.35rem 0.55rem;
  color: white;
  font-size: 0.85rem;
  cursor: pointer;
  opacity: 0;
  pointer-events: none;
  transition: opacity 0.15s ease;
}
.autoplay-controls:hover .duration { opacity: 0.9; pointer-events: auto; }
.duration:hover { opacity: 1; }
</style>
