<!-- add view attr when visible this component -->
<template>
  <div class="AnimationFadeIn">
    <div>
      <slot></slot>
    </div>
  </div>
</template>

<script>
export default {
  name: 'AnimationFadeIn'
}
</script>

<style scoped>
.AnimationFadeIn {
  position: relative;
  overflow: hidden;
  background-color: transparent;
  height: fit-content;
}

.AnimationFadeIn > * {
  position: relative;
  transition: all .8s ease-out;
  transform: translateY(100%);
}

.AnimationFadeIn[view] > * {
  transform: translateY(0); 
}

</style>
