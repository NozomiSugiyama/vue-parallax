<template>
  <div class="ParallaxBase" id="ParallaxBase">
    <slot></slot>
  </div>
</template>

<script>
export default {
  name: 'ParallaxBase'
}
</script>

<style scoped>
.ParallaxBase {
  height: 100vh;
  overflow-x: hidden;
  overflow-y: auto;
	perspective: 100px;
}
.ParallaxBase >>> * {
  transform-style: preserve-3d;
}
</style>
