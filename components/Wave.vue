<template>
  <svg class="waves" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" viewBox="0 24 150 28" preserveAspectRatio="none" shape-rendering="auto">
    <defs>
    <path id="gentle-wave" d="M-160 44c30 0 58-18 88-18s 58 18 88 18 58-18 88-18 58 18 88 18 v44h-352z" />
    </defs>
    <g class="parallax">
      <use xlink:href="#gentle-wave" x="48" y="0" fill="rgba(166,139,3, 0.7)" />
      <use xlink:href="#gentle-wave" x="48" y="3" fill="rgba(242,232,182,0.5)" />
      <use xlink:href="#gentle-wave" x="48" y="5" fill="rgba(242,203,5,0.3)" />
      <use xlink:href="#gentle-wave" x="48" y="7" fill="rgba(242,242,242)" />
    </g>
  </svg>
</template>

<style scoped>

.waves {
  position:relative;
  width: 100%;
  height:24vh;
  margin-bottom:-7px; /*Fix for safari gap*/
  min-height:100px;
}

.content {
  position:relative;
  height:20vh;
  text-align:center;
  background-color: white;
}

/* Animation */

.parallax > use {
  animation: move-forever 45s cubic-bezier(.55,.5,.45,.5)     infinite;
}
.parallax > use:nth-child(1) {
  animation-delay: -2s;
  animation-duration: 20s;
}
.parallax > use:nth-child(2) {
  animation-delay: -3s;
  animation-duration: 25s;
}
.parallax > use:nth-child(3) {
  animation-delay: -4s;
  animation-duration: 40s;
}
.parallax > use:nth-child(4) {
  animation-delay: -5s;
  animation-duration: 60s;
}
@keyframes move-forever {
  0% {
   transform: translate3d(-90px,0,0);
  }
  100% { 
    transform: translate3d(85px,0,0);
  }
}
</style>