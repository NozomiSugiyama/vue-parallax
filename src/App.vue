<template>
  <parallax-base>
    <div class="space">parallax</div>
    <div class="horizontal">
      <parallax-float :offset="0.8">
        <h3>offset 0.8</h3>
        <img src="http://placehold.jp/150x150.png">
      </parallax-float>
      <parallax-float :offset="0.6">
        <h3>offset 0.6</h3>
        <img src="http://placehold.jp/120x120.png">
      </parallax-float>
      <parallax-float :offset="0.4">
        <h3>offset 0.4</h3>
        <img src="http://placehold.jp/180x180.png">
      </parallax-float>
    </div>
    <div class="horizontal">
      <parallax-float :offset="0.2">
        <h3>offset 0.2</h3>
        <img src="http://placehold.jp/100x100.png">
      </parallax-float>
      <div>
        <h3>Normal</h3>
        <img src="http://placehold.jp/200x200.png">
      </div>
      <parallax-float :offset="-0.2">
        <h3>offset -0.2</h3>
        <img src="http://placehold.jp/180x180.png">
      </parallax-float>
    </div>
    <div class="horizontal">
      <parallax-float :offset="-0.4">
        <h3>offset -0.4</h3>
        <img src="http://placehold.jp/150x150.png">
      </parallax-float>
      <parallax-float :offset="-0.6">
        <h3>offset -0.6</h3>
        <img src="http://placehold.jp/80x80x.png">
      </parallax-float>
      <parallax-float :offset="-0.8">
        <h3>offset -0.8</h3>
        <img src="http://placehold.jp/70x70.png">
      </parallax-float>
    </div>
    <div class="space">free space</div>
  </parallax-base>
</template>

<script>
import ParallaxBase from './components/ParallaxBase.vue'
import ParallaxFloat from './components/ParallaxFloat.vue'

export default {
  name: 'app',
  components: {
    ParallaxBase,
    ParallaxFloat
  }
}
</script>

<style>
.space {
  min-height: 100vh;
  text-align: center;
  font-size: 4rem;
  display: flex;
  align-items: center;
  justify-content: center;
}

.horizontal {
  display: flex;
  flex-direction: row;
  align-items: center;
  justify-content: space-around;
}
</style>
