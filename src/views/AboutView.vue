<script setup lang="ts">
import { RouterLink } from 'vue-router'
import '../assets/cube-spinning.gif'
import '../assets/pool_boy_wikimedia.jpg'
import '../assets/masks-spin.gif'
import '../assets/mask_clnr2.gif'
import '../assets/Dido_Pollitxinella.jpg'
import '../assets/Ángel_Zárraga_-_The_Woman_and_the_Puppet_-_1909.jpg'
import '../assets/star.gif'
import '../assets/blue-crumb-1.gif'
import '../assets/Dolls_and_puppets_from_Egypt_14.jpg'
import PixelateFilter from '../components/PixelateFilter.vue'
</script>

<template>
  <PixelateFilter />
  <div class="about">
    <img src="../assets/mask_clnr2.gif" class="omage" />
    <img src="../assets/blue-crumb-1.gif" class="omage" />
    <img src="../assets/Dido_Pollitxinella.jpg" class="omage" />
    <img src="../assets/cube-spinning.gif" class="omage" />
    <img src="../assets/Ángel_Zárraga_-_The_Woman_and_the_Puppet_-_1909.jpg" class="omage" />
    <img src="../assets/star.gif" class="omage" />
    <img src="../assets/masks-spin.gif" class="omage" />
  </div>
</template>

<style scoped>
.about {
  max-width: 70vh;
  display: flex;
  flex-direction: column;
  align-items: center;
  overflow: scroll;
}
.omage {
  padding-top: 100px;
  padding-bottom: 100px;
  width: 100%;
  filter: url(#pixelate);
  cursor: url('../assets/gam416.cur'), auto;
}
</style>
