<!-- add view attr when visible this component -->
<template>
  <div class="AnimationFadeInUp">
    <div>
      <slot></slot>
    </div>
  </div>
</template>

<script>
export default {
  name: 'AnimationFadeInUp'
}
</script>

<style scoped>
.AnimationFadeInUp {
  position        : relative;
  transition      : all .6s ease-out;
  transition-delay: .3s;
}

.AnimationFadeInUp {
  opacity  : 0;
  transform: translateY(1.5rem);
}

.AnimationFadeInUp[view]{
  opacity: 1;
  bottom : 0;
  transform: translateY(0);
}

</style>
