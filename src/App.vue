<template>
  <parallax-base>
    <div class="space">parallax</div>
    <div class="horizontal">
      <parallax-float :offset="0.8">
        <h3>offset 0.8</h3>
        <img src="./assets/150x150.png">
      </parallax-float>
      <parallax-float :offset="0.6">
        <h3>offset 0.6</h3>
        <img src="./assets/120x120.png">
      </parallax-float>
      <parallax-float :offset="0.4">
        <h3>offset 0.4</h3>
        <img src="./assets/180x180.png">
      </parallax-float>
    </div>
    <div class="horizontal">
      <parallax-float :offset="0.2">
        <h3>offset 0.2</h3>
        <img src="./assets/100x100.png">
      </parallax-float>
      <div>
        <h3>Normal</h3>
        <img src="./assets/200x200.png">
      </div>
      <parallax-float :offset="-0.2">
        <h3>offset -0.2</h3>
        <img src="./assets/180x180.png">
      </parallax-float>
    </div>
    <div class="horizontal">
      <parallax-float :offset="-0.4">
        <h3>offset -0.4</h3>
        <img src="./assets/150x150.png">
      </parallax-float>
      <parallax-float :offset="-0.6">
        <h3>offset -0.6</h3>
        <img src="./assets/80x80.png">
      </parallax-float>
      <parallax-float :offset="-0.8">
        <h3>offset -0.8</h3>
        <img src="./assets/70x70.png">
      </parallax-float>
    </div>
    <div class="space">Inview</div>
    <div class="horizontal">
      <parallax-float :offset="0.4">
        <parallax-inview>
          <animation-fade-in>
            <img src="./assets/150x150.png">
          </animation-fade-in>
        </parallax-inview>
      </parallax-float>
      <parallax-float :offset="0.2">
        <parallax-inview>
          <animation-widen>
            <img src="./assets/80x80.png">
          </animation-widen>
        </parallax-inview>
      </parallax-float>
      <parallax-float :offset="0.3">
        <parallax-inview>
          <animation-widen-shadow>
            <img src="./assets/70x70.png">
          </animation-widen-shadow>
        </parallax-inview>
      </parallax-float>
    </div>
    <div class="horizontal">
      <parallax-float :offset="0.7">
        <parallax-inview>
          <animation-widen-shadow>
            <img src="./assets/100x100.png">
          </animation-widen-shadow>
        </parallax-inview>
      </parallax-float>
      <parallax-float :offset="0.4">
        <parallax-inview>
          <animation-widen-shadow>
            <img src="./assets/200x200.png">
          </animation-widen-shadow>
        </parallax-inview>
      </parallax-float>
      <parallax-float :offset="0.6">
        <parallax-inview>
          <animation-widen-shadow>
            <img src="./assets/180x180.png">
          </animation-widen-shadow>
        </parallax-inview>
      </parallax-float>
    </div>
    <div class="horizontal">
      <parallax-float :offset="0.4">
        <parallax-inview>
          <animation-widen-shadow>
            <img src="./assets/80x80.png">
          </animation-widen-shadow>
        </parallax-inview>
      </parallax-float>
      <parallax-float :offset="0.3">
        <parallax-inview>
          <animation-widen-shadow>
            <img src="./assets/150x150.png">
          </animation-widen-shadow>
        </parallax-inview>
      </parallax-float>
      <parallax-float :offset="0.5">
        <parallax-inview>
          <animation-widen-shadow>
            <img src="./assets/100x100.png">
          </animation-widen-shadow>
        </parallax-inview>
      </parallax-float>
    </div>
    <div class="space">space</div>
  </parallax-base>
</template>

<script>
import ParallaxBase from './components/parallax/ParallaxBase.vue'
import ParallaxFloat from './components/parallax/ParallaxFloat.vue'
import ParallaxInview from './components/parallax/ParallaxInview.vue'
import AnimationFadeIn from '@/components/effect/animation/AnimationFadeIn'
import AnimationWiden from '@/components/effect/animation/AnimationWiden'
import AnimationWidenShadow from '@/components/effect/animation/AnimationWidenShadow'

export default {
  name: 'app',
  components: {
    ParallaxBase,
    ParallaxFloat,
    ParallaxInview,
    AnimationFadeIn,
    AnimationWiden,
    AnimationWidenShadow
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
