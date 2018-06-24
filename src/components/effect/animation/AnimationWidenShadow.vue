<!-- add view attr when visible this component -->
<template>
  <animation-widen class="AnimationWidenShadow">
    <div>
      <slot></slot>
    </div>
  </animation-widen>
</template>

<script>
import AnimationWiden from '@/components/effect/animation/AnimationWiden'

export default {
  name: 'AnimationWidenShadow',
  components: {
    AnimationWiden
  }
}
</script>

<style scoped>
.AnimationWidenShadow {
  box-shadow: initial;
}

.AnimationWidenShadow > div {
  display: flex;
}

.AnimationWidenShadow[view] {
  position: relative;
  box-shadow: rgba(0, 0, 0, 0.3) 0px 3px 6px 2px;
  transition: box-shadow .4s ease-in-out .7s;
}

</style>
