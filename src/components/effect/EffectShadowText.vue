<template>
  <span class="EffectShadowText">
    <slot></slot>
  </span>
</template>

<script>
export default {
  name: 'EffectShadowText'
}
</script>

<style scoped>
.EffectShadowText {
  text-shadow: 2px 5px 4px #ccc;
}
</style>
