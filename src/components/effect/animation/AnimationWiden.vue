<!-- add view attr when visible this component -->
<template>
  <div class="AnimationWiden">
    <slot></slot>
    <div></div>
  </div>
</template>

<script>
export default {
  name: 'AnimationWiden'
}
</script>

<style scoped>
.AnimationWiden {
  position: relative;
  overflow: hidden;
  background-color: transparent;
}

.AnimationWiden > :not(:last-child) {
  visibility: hidden;
}

.AnimationWiden[view] > :not(:last-child) {
  animation: 0s visibility .9s;
  animation-fill-mode: forwards;
}

.AnimationWiden > :last-child {
  width: 200%;
  height: 100%;
  background-color: #333;
  top: -100%;
  left: -195%;
  position: absolute;
  z-index: 2;
}

.AnimationWiden[view] > :last-child {
  animation: .4s height .1s ease-in-out,
             .8s width .5s ease-in-out;
  animation-fill-mode: forwards;
}

@keyframes visibility {
  100% {
    visibility: visible;
  }
}

@keyframes height {
  100% {
    top: 0%;
  }
}

@keyframes width {
  100% {
    left: 100%;
  }
}
</style>
