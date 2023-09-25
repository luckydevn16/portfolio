<template>
  <section class="home-section" id="home" v-motion-fade>
    <div class="container">
      <h2 class="section-heading">Hello</h2>
      <IntroAnimation />
      <p class="section-text">
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
