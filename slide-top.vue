<template>
  <footer class="absolute bottom-0 left-0 right-0 p-2">
    <div class="absolute bottom-0 left-0 qr-wrap">
      <a :href="slideUrl" target="_blank">
        <img class="qr" :src="qrSrc" :alt="`QR to slide ${page}`" />
      </a>
    </div>
    <div class="absolute bottom-0 right-0 footer flex flex-col items-center">
      <a target="_blank" class="foot-url" href="https://tf26.hccs.dev">tf26.hccs.dev</a>
      <a target="_blank" href="https://hudcostreets.org"><div class="foot-logo"/></a>
    </div>
  </footer>
</template>
<script setup lang="ts">
import { computed } from 'vue'
import { useNav } from '@slidev/client'

const { currentSlideNo } = useNav()
const page = computed(() => currentSlideNo.value)
const qrSrc = computed(() => `/qr/${String(page.value).padStart(2, '0')}.svg`)
const slideUrl = computed(() => `https://tf26.hccs.dev/${page.value}`)
</script>
<style scoped>
.qr-wrap {
  padding: 0.4rem;
}
.qr {
  width: 4.4rem;
  height: 4.4rem;
  display: block;
  background: white;
  padding: 0.2rem;
  border-radius: 0.25rem;
}
</style>
