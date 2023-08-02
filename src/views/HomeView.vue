<template>
  <section class="home-section" id="home" v-motion-fade>
    <div class="container">
      <h2 class="section-heading">Hello</h2>
      <IntroAnimation />
      <p class="section-text">
        My name is {{ heroName }}, I'm a {{heroActivity}} based in {{ heroFrom }}. <br>
        {{heroMemo01}}<br>
        {{heroMemo02}}
      </p>
    </div>
  </section>
</template>

<script>
import IntroAnimation from '@/components/IntroAnimation.vue'

export default {
  name: 'HomeView',
  components: {
    IntroAnimation
  },
  data() {
    return {
      heroName: process.env.VUE_APP_HERO_NAME,
      heroActivity: process.env.VUE_APP_HERO_ACTIVITY,
      heroFrom: process.env.VUE_APP_HERO_FROM,
      heroMemo01: process.env.VUE_APP_HERO_MEMO_01,
      heroMemo02: process.env.VUE_APP_HERO_MEMO_02
    };
  }
}
</script>

<style>
.home-section .section-heading {
  color: var(--home-color);
}
</style>
