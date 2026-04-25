---
theme: ./theme
title: Data-Driven Advocacy
info: Hudson County Complete Streets — North Jersey Transit Forum, 4/25/26
selectable: true
class: text-center  # apply unocss classes to the current slide
colorSchema: dark
drawings:  # https://sli.dev/features/drawing
  persist: false
mdc: true
layout: section
---

# Data-Driven Advocacy

North Jersey Transit Forum, 4/25/26

Ryan Williams

Hudson County Complete Streets

<!--
[hudcostreets.org](https://hudcostreets.org)

Slides: [tf26.hccs.dev](https://tf26.hccs.dev)
-->

---
class: hccs
dragPos:
  bp: 620,20,220,73
  blr: 620,103,220,132
  bb: 620,245,220,132
  vz: 620,387,220,124
---

<style>
.slidev-layout.hccs {
  padding-top: 1.5rem;
  padding-left: 2.7rem;
  h1 {
    max-width: 540px;
    margin-bottom: 0.2rem;
    font-size: 1.7rem;
    line-height: 2rem;
  }
  p { margin: 0.4rem 0; }
  li { line-height: 1.5rem }
  blockquote { width: 50% !important; font-size: 0.9rem; }
  .body {
    width: 52%;
    font-size: 0.92rem;
    p:first-child { margin-top: 0; }
    li {
      line-height: 1.5rem !important;
    }
  }
  .tile {
    text-align: center;
  }
  .tile a {
    display: block;
    width: 100%;
    height: 100%;
    text-decoration: none !important;
    border: none !important;
  }
  .tile img {
    width: 100%;
    height: 100%;
    object-fit: contain;
    background: white;
    border-radius: 4px;
  }
  .tile img[src*="logo"] {
    background: white;
    padding: 4px;
  }
}
</style>


# Hudson County Complete Streets
> Our mission is to improve mobility in Hudson County by advocating for **safe streets**, pedestrian and cycling **infrastructure**, and **access to transit.**

<div class="body">

500+ volunteers · 8K newsletter · 9-member board · 2 part-time staff

4 major campaigns:
- [Better PATH][PATH] — 7,000+ signatures
- [Better Light Rail][HBLR] — **sign the petition!**
- [Better Buses][BB] (BRT on JFK)
- [Vision Zero][VZ] — HC Safety Action Plan

Recent wins:
- 🎉 [PATH service improvements][path-win] (Nov '25)
- 🎉 [Turnpike: 1 bridge instead of 2][tt-win] (Mar '26)

Also: [Viaduct], [JFK Blvd E] — 👉 [hudcostreets.org]
</div>

<div v-drag="'bp'" class="tile"><a href="https://hudcostreets.org/panynj" target="_blank"><img src="/better-path-logo.png"/></a></div>
<div v-drag="'blr'" class="tile"><a href="https://hudcostreets.org/hblr" target="_blank"><img src="/better-light-rail-logo.png"/></a></div>
<div v-drag="'bb'" class="tile"><a href="https://hudcostreets.org/better-buses" target="_blank"><img src="/better-buses-hero.webp"/></a></div>
<div v-drag="'vz'" class="tile"><a href="https://hudcostreets.org/vision-zero" target="_blank"><img src="/vision-zero-logo.webp"/></a></div>

[PATH]: https://hudcostreets.org/panynj
[HBLR]: https://hudcostreets.org/hblr
[BB]: https://hudcostreets.org/better-buses
[Viaduct]: https://hudcostreets.org/viaduct
[JFK Blvd E]: https://hudcostreets.org/jfkblvdeastredesign
[VZ]: https://hudcostreets.org/vision-zero
[path-win]: https://hudcostreets.org/news/press-release-path-win
[tt-win]: https://hudcostreets.org/news/praiseforturnpikeextensionrepairplan

[hudcostreets.org]: https://hudcostreets.org/

---
class: plots
dragPos:
  hom: 16,75,215,148
  sp: 16,234,215,148
  path: 16,393,215,147
  jc: 241,73,185,242
  hc: 241,325,185,216
  xbl: 436,21,331,267
  cb-m: 436,298,331,242
  cb: 777,20,192,124
  cb-r: 777,154,192,120
  cb-g: 777,286,192,120
  cb-u: 777,418,192,120
---

<style>
.slidev-layout.plots {
  & + footer { display: none }
  padding-top: 1.3rem;
  padding-left: 1.2rem;
  img {
    width: 100%;
    height: 100%;
  }
}
</style>

<div v-drag="'hom'" ><a target="_blank" href="https://crashes.hudcostreets.org/#vs-homicides"><img src="/hom.png"/></a></div>
<div v-drag="'sp'"  ><a target="_blank" href="https://crashes.hudcostreets.org/#per-year"><img src="/njsp.png"/></a></div>
<div v-drag="'path'"><a target="_blank" href="https://path.hudcostreets.org/#vs-2019"><img src="/path-vs19.png"/></a></div>
<div v-drag="'jc'"  ><a target="_blank" href="https://map.bikejc.org/?ll=40.720_-74.068&z=14"><img src="/jc.gif" /></a></div>
<div v-drag="'hc'"  ><a target="_blank" href="https://crashes.hudcostreets.org/map/hudson"><img src="/hc-map.png"/></a></div>
<div v-drag="'xbl'" ><a target="_blank" href="https://github.com/hudcostreets/hudson-transit"><img src="/xbl.png"/></a></div>
<div v-drag="'cb-m'"><a target="_blank" href="https://ctbk.dev/stations?ll=40.717-74.045&z=15&ss=JC115&ym=2410"><img src="/g2410.png"/></a></div>
<div v-drag="'cb'"  ><a target="_blank" href="https://ctbk.dev/"><img src="/cb.png"/></a></div>
<div v-drag="'cb-r'"><a target="_blank" href="https://ctbk.dev/?s=b&pct&rt=ce&d=2002-"><img src="/cb-r.png"/></a></div>
<div v-drag="'cb-g'"><a target="_blank" href="https://ctbk.dev/?y=m&s=g&pct&g=mf&d=1406-2102"><img src="/cb-g.png"/></a></div>
<div v-drag="'cb-u'"><a target="_blank" href="https://ctbk.dev/?s=u&pct"><img src="/cb-u.png"/></a></div>

## Transportation data projects

[hom-cmp]: https://crashes.hudcostreets.org/#vs-homicides
[xbl]: https://github.com/hudcostreets/hudson-transit
[grove-2410]: https://ctbk.dev/stations?ll=40.717-74.045&z=15&ss=JC115&ym=2410
[path]: https://path.hudcostreets.org/#vs-2019

---
class: us
---
<style>
.slidev-layout.us {
  padding-right: 5rem;
  h2 {
    margin-top: 1.7rem;
    margin-bottom: 0.5rem;
  }
  .right-overlay {
    padding: 2rem;
  }
}</style>

# US transportation is too car-dependent — and we're falling behind

- US trails peer countries on transit investment, road safety, and per-capita VMT
- [Worse mobility][cn hsr], hollowed-out cities, [\$TNs][debt] of auto debt, [\$TNs][insurance] of auto insurance

## Theory of change
- **Data for decision-making** — sensors + open data + analysis tools
- **Internet / social media** — shows what's possible, enables organizing
- **New technology** — ebikes/micromobility, faster transit, can reduce car dependence

[debt]: https://www.lendingtree.com/auto/debt-statistics/
[insurance]: https://www.statista.com/outlook/fmo/insurances/non-life-insurances/motor-vehicle-insurance/united-states
[cn hsr]: https://www.threads.net/@thetransitguy/post/DGY0GP6B3hD/video-this-is-the-beijing-shanghai-corridor-which-takes-4-hours-and-18-minutes-to-cove

<a target="_blank" href="https://www.thetransportpolitic.com/2023/06/07/once-a-leader-in-urban-rail-investment-the-united-states-now-trails/"><img v-click class="right-overlay" src="/subway-countries.jpeg"/></a>

<a target="_blank" href="https://www.nytimes.com/2022/11/27/upshot/road-deaths-pedestrians-cyclists.html"><img v-click class="right-overlay" src="/deaths-per-capita.png"/></a>


---
class: opps0
dragPos:
  cars: 396,125,565,_
  mode: 54,173,889,_
  intra: 54,192,840,_
  weather: 28,248,558,_
  bike: 595,20,364,_
---

<style>
.opps0 {
  &+footer { display: none; }
  .slidev-vclick-hidden { display: none; }
  padding-left: 2rem;
  .left {
    width: 50%;
  }
}
</style>

# Hudson County – the opportunity

700K residents, 12 munis — **the size and density of Boston**.

<div v-click="[0,1]">
<div v-drag="'mode'"><a href="https://www.njtpa.org/NJTPA/media/Documents/Data-Maps/Modeling-Surveys/Household-Travel-Survey/RHTS_Hudson_f1.pdf" target="_blank"><img src="/njtpa-hc-modes.png" /></a></div>
</div>

- < 50% of trips by car, today (only non-NYC US county)
- **92%** of NJ→NYC commuters travel by transit
<div v-click="[1,2]">
<div v-drag="'cars'"><a href="https://github.com/hudcostreets/household-vehicles/tree/main/hudson#vehicles-per-household-hudson-county" target="_blank"><img src="/hc_vehs_years_title.png" /></a></div>
</div>
<div v-click="[1,2]">

- 33% of households car-free
</div>
<div v-click="[2,3]">

- 68% of trips are within Hudson County
</div>
<div v-click="[2,3]">
<div v-drag="'intra'"><a href="https://www.njtpa.org/NJTPA/media/Documents/Data-Maps/Modeling-Surveys/Household-Travel-Survey/RHTS_Hudson_f1.pdf" target="_blank"><img src="/njtpa-intra-hc-crop.png" /></a></div>
</div>
<div v-click="3" class="left">

- Perfect size, density, weather for micromobility (bikes, e-bikes, scooters)
</div>
<div v-click="3">
<div v-drag="'weather'"><img src="/hc-weather.png" /></div>
<div v-drag="'bike'"><img src="/hc-bike-len.png" /></div>
</div>

---
layout: section
class: bus-section
---

<style>
.bus-section {
  &+footer { display: none; }
  display: flex !important;
  align-items: center;
  justify-content: center;
  img {
    display: inline;
    max-width: 75%;
    max-height: 80vh;
    border-radius: 6px;
  }
}
</style>

<a href="https://hudcostreets.org/better-buses" target="_blank"><img src="/better-buses-hero.webp" /></a>

---
class: brt
dragPos:
  jfk: 568,18,402,_
  cost: 13,311,669,_
---

<style>
.brt {
  &+footer { display: none; }
  .jfk { z-index: 1 !important; }
  img[src*="cost"] { z-index: 20 !important; }
  video {
    height: 100%;
    position: absolute;
    bottom: 0;
    right: 0;
    z-index: 10;
  }
}
</style>
# BRT on JFK
- Bus Rapid Transit: bus lanes, signal priority, etc.
- Ridership could ≈ a subway line (**10-20x** a car lane)


<div v-click="1">
<video src="/42-brt.mp4" controls loop autoplay muted />

- Can double as bike/ebike/scooter lane
  - Gets them off sidewalk!
</div>

<div v-drag="'jfk'" class="jfk"><a href="https://www.hcnj.us/wp-content/uploads/2022/02/JFK_Study-Report_Final.pdf" target="_blank"><img src="/jfk-map.png" /></a></div>
<div v-click="2">
<div v-drag="'cost'"><a href="https://www.hcnj.us/wp-content/uploads/2022/02/JFK_Study-Report_Final.pdf" target="_blank"><img src="/jfk-crash-cost.png" /></a></div>

- Crashes on JFK are expensive
  - $27MM/yr directly from crashes
  - [$200MM/yr][JFK] total ‼️
</div>

[JFK]: https://www.hcnj.us/wp-content/uploads/2022/02/JFK_Study-Report_Final.pdf

---
class: xbl
dragPos:
  xbl: 350,40,540,360
---

<style>
.xbl {
  &+footer { display: none; }
  .col-left { width: 25%; }
}
</style>
<div class="col-left">

## [Lincoln Tunnel Bus Lane](https://www.panynj.gov/bridges-tunnels/en/lincoln-tunnel/xbl.html)

<br/>

> … busiest and most productive highway lane in the nation, moving over 1,850 buses and 70,000 passengers each weekday morning &nbsp;[<mdi-link />][xbl faq]

1 bus lane moves **5x** as many people per hour…

as 5 car lanes (Lincoln+Holland) _combined_ 🤯.

95% of Holland Tunnel vehicles are cars

80% have 1 person
</div>

[xbl]: https://www.panynj.gov/bridges-tunnels/en/lincoln-tunnel/xbl.html
[xbl faq]: https://www.panynj.gov/port-authority/en/help-center/faq/bridges-and-tunnels-faq.html

<div v-drag="'xbl'"><a href="https://hbt.hccs.dev" target="_blank"><img src="/hbt-bubble-1h.png"/></a></div>

---
class: hbt-map
---

<style>
.slidev-layout.hbt-map {
  &+footer { display: none; }
  padding: 0;
  background: black;
  position: relative;
  a {
    position: absolute;
    inset: 0;
    display: block;
  }
  img {
    width: 100%;
    height: 100%;
    object-fit: contain;
    display: block;
  }
}
</style>

<a href="https://hbt.hccs.dev" target="_blank"><img src="/hbt-map-nj-ny.png" /></a>

---
class: deaths
dragPos:
  plot: 20,218,370,_
  stats: 397,217,224,_
  map: 629,92,342,_
---

<style>
.deaths {
  &+footer { display: none; }
  padding: 1.4rem 0 0 2rem;
  h1 {
    margin-bottom: 0.3rem;
    font-size: 1.7rem;
    line-height: 2rem;
    max-width: 65%;
  }
  .body {
    width: 60%;
    font-size: 0.92rem;
    li { line-height: 1.4rem; }
    p { margin: 0.3rem 0; }
  }
  img {
    width: 100%;
    height: 100%;
    object-fit: contain;
  }
  .link {
    position: absolute;
    right: 1rem;
    bottom: 0;
    font-size: 0.9rem;
  }
}
</style>

# Hudson County – Deaths, Injuries, Property Damage

<div class="body">

Car crashes kill more people **than murders** — **1.6× more in 2023**, 1.1× since 2018.

- 50 crashes per day (reported to police).
- Per year:
  - 23 deaths (9 pedestrians, 10 drivers, 2 passengers, 1-2 cyclists)
  - 150 serious injuries, 1,000-4,000 other injuries
</div>

<div v-drag="'plot'"><a href="https://crashes.hudcostreets.org/c/hudson" target="_blank"><img src="/hc-traffic-deaths.png" /></a></div>
<div v-drag="'stats'"><a href="https://crashes.hudcostreets.org/c/hudson/#stats" target="_blank"><img src="/hc-crash-stats.png" /></a></div>
<div v-drag="'map'"><a href="https://crashes.hudcostreets.org" target="_blank"><img src="/hc-crash-map.png" /></a></div>

<div class="link">

[crashes.hudcostreets.org](https://crashes.hudcostreets.org)
</div>

---
class: cars
dragPos:
  cars: 415,88,555,_
---

<style>
.cars {
  &+footer { display: none; }
  .slidev-vclick-hidden { display: none; }
  padding-left: 2rem;
  .left {
    width: 42%;
  }
}
</style>

# Cost of car-dependence
277k cars in Hudson County:
<div class="left">

- **≈$3BN / year** buying, insuring, maintaining
- **≈$2BN auto debt** ($1TN nation-wide)
- **10% increase** since COVID ‼️

<br/>
<div v-click>
Traffic and parking will only get worse, if the number of cars keeps rising.
</div>
<br/>
<div v-click>
People need (and want) transportation alternatives…
</div>
</div>
<div v-click>
<br/>

["D" air quality grade…][ALA]
</div>

<div v-drag="'cars'"><a href="https://github.com/hudcostreets/household-vehicles/tree/main/hudson#vehicles-per-household-hudson-county" target="_blank"><img src="/hc_vehs_title.png" /></a></div>

[ALA]: https://www.lung.org/research/sota/city-rankings/states/new-jersey/hudson

---
class: wt
dragPos:
  wt: 366,211,297,_
  bb1: 196,17,385,_
  bb2: 580,16,392,_
---

<style>
.wt {
  &+footer { display: none; }
  .body {
    width: 75%;
    margin-bottom: .5rem;
  }
  & > div:nth-child(2) {
    margin-top: 0;
  }
  video.wt-vid {
    border: 1rem solid #00793f;
    border-left: none;
    position: absolute;
    right: 0;
    bottom: 0;
    height: 100%;
  }
  .left {
    width: 36%;
    &.inner > ul > li { list-style: none; }
  }
}
</style>

# [Jersey City Ward Tour][wt]

<div class="body">

The **busiest hour of the year** on JFK Blvd and Rt 139:<br/>2,000 cyclists, rolling closures of 5-30 mins.
</div>

<div class="left">

- 16 miles, 6 wards
- JFK: 25,000 vehicles/day, ≤2,000/hr
</div>

<video class="wt-vid" src="/wt.mp4" autoplay muted loop controls />

<div class="left">

Children can bike from downtown to Greenville to West Side to Heights and back — **when we make it safe**.
</div>

<div v-drag="'wt'"><a href="https://www.bikejc.org/ward-tour" target="_blank"><img src="/wt.png" /></a></div>

[wt]: https://www.bikejc.org/ward-tour
<div v-click class="left">
<div v-drag="'bb2'"><a href="https://instagram.com/jcbikebus" target="_blank"><img src="/bike-bus2.jpeg" /></a></div>
<div v-drag="'bb1'"><a href="https://instagram.com/jcbikebus" target="_blank"><img src="/bike-bus1.jpeg" /></a></div>
</div>

---
class: cycling-growth
---

<style>
.slidev-layout.cycling-growth {
  &+footer { display: none; }
  padding: 0.6rem 1rem 0 1rem;
  text-align: center;
  h1 {
    margin: 0 0 0.3rem 0;
    font-size: 1.4rem;
  }
  a img {
    max-width: 96%;
    max-height: 78vh;
    display: inline-block;
    border-radius: 4px;
  }
  .src {
    font-size: 0.7rem;
    opacity: 0.7;
    margin-top: 0.3rem;
  }
}
</style>

# Cycling mode shift

<a href="https://www.tandfonline.com/doi/full/10.1080/15568318.2026.2649315" target="_blank"><img src="/cycling-mode-share-4cities.png" /></a>

<div class="src">

Buehler, Pucher, Moran, de Lanversin, Aldred (Apr '26), [Int'l J. of Sustainable Transportation](https://www.tandfonline.com/doi/full/10.1080/15568318.2026.2649315)
</div>

---
layout: iframe-right
url: https://ctbk.dev
scale: 0.8
class: ctbk
---
<style>
.ctbk + footer { display: none; }
.slidev-layout.ctbk {
  padding: 2rem 1rem 0 2rem;
  p { margin-bottom: 0.5rem }
  li { line-height: 1.75rem }
  img:not(.right-overlay) {
    height: 14.8rem;
    position: absolute;
    padding-left: 1rem;
    bottom: 1rem;
    z-index: 1;
  }
  .right-overlay {
    border: 1rem solid #00793f;
    border-left: none;
  }
}
</style>

# Bike Share
- **10,000 trips per day** achievable in **5 years**
  - Largely replacing car trips
  - Cheaper, cleaner, quieter, safer mobility
- Grove St (≈5 car-parking spots): **300 rides per day**
- JC+HOB: [63%][ebikes] ebike share, [78%][subs] annual members

[![](/g2505.png)][2505]

<img class="right-overlay" src="/cb-opp2.png" />

<!--
Show JC+HOB plateau, ebike share over time, Grove St 80/day in Feb '25
Show station map by add date
-->

[ctbk.dev]: https://ctbk.dev
[`s3://ctbk`]: https://ctbk.s3.amazonaws.com/index.html
[`s3://tripdata`]: https://tripdata.s3.amazonaws.com/index.html
[cb data]: https://www.citibikenyc.com/system-data
[ctbk gh]: https://github.com/hudcostreets/ctbk.dev
[2505]: https://ctbk.dev/stations?ll=40.717-74.045&z=15&ss=JC115&ym=2505
[ebikes]: https://ctbk.dev/?s=b&pct&rt=ce&d=2002-&r=jh
[subs]: https://ctbk.dev/?s=u&pct&r=jh

---
layout: iframe-right
url: https://map.bikejc.org/?l=wbr
class: jc
dragPos:
  bb: 18,218,457,_
  bbl: 443,378,261,_
---

<style>
.jc {
  &+footer { display: none }
  .bb p {
    position: relative;
    z-index: 100;
  }
  img[src*="map"] {
    z-index: 1 !important;
  }
}
</style>

# Bike infrastructure
- Jersey City: ≈2,000 lane-miles for cars, ≈20 miles of protected bike lanes
  - [JC Bike Master Plan][bmp] / [bikejc.github.io/bike-master-plan] / [PDF]

<div v-click class="bb">
<div v-drag="'bb'"><a href="https://dev.bikejc.org/bike-bus/map" target="_blank"><img src="/bb-map.png" /></a></div>
<div v-drag="'bbl'"><a href="https://dev.bikejc.org/bike-bus" target="_blank"><img src="/bb-lines.png" /></a></div>

[Bike bus (2023)][bb]:
</div>

[bb]: https://dev.bikejc.org/bike-bus/
[map.bikejc.org]: https://map.bikejc.org
[bmp]: https://street-plans.com/lets-ride-jc-bicycle-master-plan-jersey-city-nj/
[bikejc.github.io/bike-master-plan]: https://bikejc.github.io/bike-master-plan/
[PDF]: https://cdn5-hosted.civiclive.com/UserFiles/Servers/Server_6189660/File/Community/Transportation/LetsRideJCMasterPlan-FinalDraft%206.16.19_09_30.pdf

---
class: ht
---

<style>
.slidev-layout.ht {
  &+footer { display: none; }
  padding: 1.4rem 0 0 1.5rem;
  h1 {
    max-width: 285px;
    margin-bottom: 0.4rem;
    font-size: 1.55rem;
    line-height: 1.85rem;
  }
  .col-left {
    width: 285px;
    font-size: 0.85rem;
    li { line-height: 1.3rem; }
    p { margin: 0.35rem 0; }
  }
  video {
    position: absolute;
    top: 1.4rem;
    right: 1.5rem;
    width: 640px;
    height: auto;
    border: 1px solid white;
  }
}
</style>

# [Holland Tunnel bike share][ht]

<div class="col-left">

[ht.hccs.dev][ht]: **1 of 2 lanes** open to bikes for **10 minutes per hour**.

- E/b and W/b alternate, offset 30 mins
- "Pace" + "Sweep" cars manage transitions
- ≈600 bikes/hour of new capacity
  - vs. ≈1,500 cars/hr today

Holland is the only NJ↔NYC crossing without a transit/bike option.
</div>

<a href="https://ht.hccs.dev" target="_blank"><video src="/ht.mp4" autoplay muted loop controls /></a>

[ht]: https://ht.hccs.dev

---
class: vd
dragPos:
  guy: 500,36,383,_
  vd0: 32,126,441,_
  vd1: 32,336,441,_
---

<style>
.vd {
  &+footer { display: none; }
  .slidev-vclick-hidden { display: none; }
  padding-left: 2rem;
  h1 { margin-bottom: 0.5rem; }
  video {
    height: 100%;
    position: absolute;
    bottom: 0;
    right: 0;
    z-index: 10;
  }
  .drag {
    width: 45%;
  }
}
</style>

# Bike infrastructure
[Viaduct multi-use path][vd]!

<video src="/viaduct.mov" controls loop autoplay muted />

<div class="drag" v-drag="'vd0'"><a href="https://streetmix.net/streetmix-7762/16/14th-st-viaduct-current" target="_blank"><img src="/vd0.png" /></a></div>
<div class="drag" v-drag="'vd1'"><a href="https://streetmix.net/streetmix-7762/15/14th-st-viaduct-proposed" target="_blank"><img src="/vd1.png" /></a></div>
<div v-click>
<div class="drag" v-drag="'guy'"><a href="https://www.hcnj.us/blog/2025/05/22/15886/" target="_blank"><img src="/vd-pr.png" /></a></div>
</div>

[vd]: https://www.hcnj.us/blog/2025/05/22/15886/

---
class: ebikes
dragPos:
  bunch: 342,285,350,_
  baboe: 643,-1,339,_
  bh: 93,264,483,_
  nyc: 764,-2,217,_
  dot: 576,264,402,_
---

<style>
.ebikes {
  padding-top: .8rem;
}
</style>

# Micromobility (e-bikes / scooters)

- Best-selling electric vehicles in the US
- Cheaper, cleaner, quieter, **safer**, faster alternatives to driving
<div v-click="1">

<ul><li style="list-style: none">

  - NJ: **0** pedestrian deaths from e-bikes, **ever** (vs. **100's/year by cars**)
  - Bike Hoboken: 0 crash reports re: (e)bikes on sidewalks
  - Better infrastructure + enforcing existing laws = safer streets
</li></ul>
</div>
<div v-click="2">

- 💡 E-bike rebate/voucher programs
</div>

<div v-drag="'bunch'"><img src="/bunch.jpg" /></div>
<div v-drag="'baboe'"><img src="/baboe.jpg" /></div>

<div v-click="1">
<div v-drag="'bh'"><a href="https://www.bikehoboken.org/articles/2024-bike-hoboken-traffic-injury-report" target="_blank"><img src="/bh.png" /></a></div>
<div v-drag="'nyc'"><a href="https://nyc.streetsblog.org/2025/06/10/now-do-cars-adams-and-council-push-for-e-bike-speed-limits-ignores-the-biggest-danger" target="_blank"><img src="/nyc-ebikes.png" /></a></div>
<div v-drag="'dot'"><a href="https://www.nyc.gov/html/dot/html/bicyclists/bikestats.shtml#crashdata" target="_blank"><img src="/nyc-dot.jpg" /></a></div>
</div>

---
class: jct
dragPos:
  jct: 380,40,590,_
---

<style>
.slidev-layout.jct {
  &+footer { display: none; }
  padding: 1.4rem 0 0 1.5rem;
  h1 {
    max-width: 340px;
    margin-bottom: 0.4rem;
    font-size: 1.55rem;
    line-height: 1.85rem;
  }
  .col-left {
    width: 340px;
    font-size: 0.85rem;
    li { line-height: 1.3rem; }
    p { margin: 0.35rem 0; }
  }
}
</style>

# [JC property taxes][jct] — TOD pays for transit

<div class="col-left">

- JC has a **$250MM/yr deficit** (and rising)
- Single downtown towers pay **$10MM/yr** in property tax
- Parking lots & low-rise next to transit ≈ wasted land

[jct.rbw.sh][jct]: every property tax payment, 2018-2025, mapped to its parcel.

→ Build more housing, **especially near transit**.<br/>
→ TOD = density = revenue = more transit.
</div>

<div v-drag="'jct'"><a href="https://jct.rbw.sh" target="_blank"><img src="/jct-west.png" /></a></div>

[jct]: https://jct.rbw.sh

---
class: srcs
---

<style>
.slidev-layout.srcs {
  &+footer { display: none; }
  padding: 1.5rem 1.5rem 0 1.5rem;
  h1 { margin-bottom: 0.5rem; font-size: 1.6rem; }
  table { font-size: 0.78rem; line-height: 1.2rem; }
  th, td { padding: 0.25rem 0.5rem !important; }
}
</style>

# Data sources

| Agency      | Data                               | Frequency  | Delay | Mirror / Site                                                                                                                |
|-------------|------------------------------------|------------|-------|------------------------------------------------------------------------------------------------------------------------------|
| [NJSP]      | Crashes (fatal)                    | Daily      | 1d–3mos | [<logos-github-icon/>][hudcostreets/nj-crashes] [<logos-aws-s3 />][`s3://nj-crashes/njsp`] &nbsp;[crashes.hudcostreets.org] |
| [NJ DOT]    | Crashes (all)                      | Annually   | 2-3yrs ('23) | [<logos-github-icon/>][hudcostreets/nj-crashes] [<logos-aws-s3 />][`s3://nj-crashes/njdot`] &nbsp;[crashes.hudcostreets.org] |
| [Lyft]      | Citi Bike ridership                | Monthly    | ≈1wk  | [<logos-github-icon/>][hudcostreets/ctbk.dev] [<logos-aws-s3 />][`s3://ctbk`]                &nbsp;[ctbk.dev]                |
| [PANYNJ]    | PATH ridership                     | Monthly    | 1-2mos | [<logos-github-icon/>][hudcostreets/path]                                                    &nbsp;[path.hudcostreets.org]   |
| [NYMTC]     | Hudson River crossings             | Annually   | 1-2yrs ('24) | [<logos-github-icon/>][hudcostreets/hudson-transit] [<logos-google-drive />][HCCS NYMTC]                                     |
| NJ Transit  | Rides per station/line             | OPRA       | -     | [<logos-google-drive />][HCCS NJT]                                                                                           |
| NJ Turnpike | Exits × Veh types                  | OPRA       | -     | [<logos-google-drive />][HCCS NJTA]                                                                                          |
| [Lyft]      | [Citi Bike system status][cb gbfs] | Realtime ([GBFS]) | 1min | -                                                                                                                            |
| PANYNJ      | [PATH real-time status][path realtime] | Realtime ([GTFS]) | 1min | [<logos-github-icon/>][mrazza/path-data] &nbsp;[<logos-github-icon/>][jamespfennell/path-train-gtfs-realtime]                |

[ctbk.dev]: https://ctbk.dev
[crashes.hudcostreets.org]: https://crashes.hudcostreets.org
[path.hudcostreets.org]: https://path.hudcostreets.org
[hudcostreets/hudson-transit]: https://github.com/hudcostreets/hudson-transit

[NJSP]: https://www.nj.gov/njsp/info/fatalacc/index.shtml
[NJ DOT]: https://www.nj.gov/transportation/refdata/accident/rawdata01-current.shtm
[PANYNJ]: https://www.panynj.gov/path/en/about/stats.html
[NYMTC]: https://www.nymtc.org/en-us/Data-and-Modeling/Transportation-Data-and-Statistics/Publications/Hub-Bound-Travel
[Lyft]: https://citibikenyc.com/system-data

[`s3://nj-crashes/njsp`]: https://nj-crashes.s3.amazonaws.com/index.html#/njsp/data
[`s3://nj-crashes/njdot`]: https://nj-crashes.s3.amazonaws.com/index.html#/njdot/data
[hudcostreets/path]: https://github.com/hudcostreets/path
[hudcostreets/nj-crashes]: https://github.com/hudcostreets/nj-crashes
[hudcostreets/ctbk.dev]: https://github.com/hudcostreets/ctbk.dev
[HCCS NYMTC]: https://drive.google.com/drive/folders/1Dm-ZBYxWaOaGgm08XCGOZCuvU2IQaPLN
[HCCS NJTA]: https://drive.google.com/drive/folders/1Ff4TUP6MmuoGvE0qTE2cgBukoxstB-93
[HCCS NJT]: https://drive.google.com/drive/folders/1IkeX8EOavWC1uUa1eHIIbVmE8i5tDuwE
[`s3://ctbk`]: https://ctbk.s3.amazonaws.com/index.html

[GBFS]: https://github.com/MobilityData/gbfs
[cb gbfs]: https://gbfs.citibikenyc.com/gbfs/2.3/gbfs.json
[GTFS]: https://gtfs.org/

[path realtime]: https://www.panynj.gov/path/en/index.html
[mrazza/path-data]: https://github.com/mrazza/path-data
[jamespfennell/path-train-gtfs-realtime]: https://github.com/jamespfennell/path-train-gtfs-realtime

---
layout: section
class: end
---

# Thank you!

<!--
TODO:
- Eli Bender
- TurnpikeTrap
- JSQ
- Trees crash
- Viaduct streetmixes

- glowy crash map 2022 update
- Specify HC in homs plot
  - Add statewide click
- Link "deaths" plots
- more cargobike photos
-->
