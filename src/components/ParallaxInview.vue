<!-- add view attr when visible this component -->
<template>
  <div class="ParallaxInview" :view="isView">
    <slot></slot>
  </div>
</template>

<script>
export default {
  name: 'ParallaxInview',
  data: () => ({
    isView: false,
    scrollEvent: () => undefined
  }),
  mounted: function() {
    const base = document.getElementById("ParallaxBase")
    this.scrollEvent = () => {
      const rect = this.$el.getBoundingClientRect()

      if (rect.top < window.innerHeight) {
        this.isView = true;
        for (let slot of this.$slots.default)
          slot.elm instanceof HTMLElement && slot.elm.setAttribute('view', true)
      } else {
        this.isView = false;
        for (let slot of this.$slots.default)
          slot.elm instanceof HTMLElement && slot.elm.removeAttribute('view')
      }
    }
    this.scrollEvent()
    base.addEventListener('scroll', this.scrollEvent)
  },
  destroyed: function () {
    const base = document.getElementById("ParallaxBase")
    base.removeEventListener('scroll', this.scrollEvent)
  }
}
</script>

<style scoped>
.ParallaxInview {
  
}
</style>
