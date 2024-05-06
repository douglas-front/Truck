<script setup lang="ts">
import hero from './components/hero/hero.vue'
import SecondSection from './components/SecondSection/SecondSection.vue';
import Nav from './components/Nav/Nav.vue';

</script>

<template>
  <main ref="container" data-scroll-container>
    <Nav/>
    <hero />
    <SecondSection />
  </main>
</template>
