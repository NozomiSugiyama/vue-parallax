<template>
  <div class="ParallaxFloat" :style="style">
    <slot></slot>
  </div>
</template>

<script>
export default {
  name: 'ParallaxFloat',
  data: () => ({
    style: undefined,
  }),
  props: {
    offset: {
      default: 0.3,
      type: Number
    },
  },
  mounted: function() {
    const rect = this.$el.getBoundingClientRect()

    const left = ((window.innerWidth / 2) - rect.left - (rect.width / 2) ) * this.offset;
    console.log((window.innerWidth / 2) - rect.left)
    console.log((rect.width / 2) )
    const translateZ = this.offset * 100;
    this.style={ left: `${left}px`, transform: `translateZ(${translateZ}px) scale(${1 - this.offset})`, zIndex: `${this.offset * 10}` }
  },
}
</script>

<style scoped>
.ParallaxFloat {
  transform-style: preserve-3d;
  position: relative;
}
</style>
