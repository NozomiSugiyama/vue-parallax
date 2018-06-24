<template>
  <div class="EffectShadow">
    <slot></slot>
  </div>
</template>

<script>
export default {
  name: 'EffectShadow'
}
</script>

<style scoped>
.EffectShadow {
  position: relative;
  box-shadow: rgba(0, 0, 0, 0.3) 0px 3px 6px 2px;
}
</style>
