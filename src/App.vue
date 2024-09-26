<script setup>
import Navbar from './components/Navbar.vue';
import Hero from './components/Hero.vue';
import Cards from './components/Cards.vue';
import Cards2 from './components/Cards2.vue';


</script>

<template>
  <header>
    <Navbar />
    <Hero />
    <Cards />
    <Cards2 />
 
  </header>

 
</template>

<style scoped>
.hero-section {
  background-image: url('@/assets/img/image.jpeg');
  background-size: cover;
  background-position: center;
  height: 50vh;
  
}

</style>

