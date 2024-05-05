<script lang="ts">
import LocomotiveScroll from 'locomotive-scroll'
import hero from './components/hero/hero.vue'
import SecondSection from './components/SecondSection/SecondSection.vue';
import Nav from './components/Nav/Nav.vue';
export default {
  methods: {
    setLocomotiveScroll() {
      new LocomotiveScroll({
        el: this.$refs.container as HTMLElement,
        smooth: true,
        multiplier: 1
      })
    }
  },
  mounted() {
    this.setLocomotiveScroll()
  },
  components: {
    hero,
    SecondSection,
    Nav
  }
}
</script>

<template>
  <main ref="container" data-scroll-container>
    <Nav/>
    <hero />
    <SecondSection />
  </main>
</template>
