<script setup lang="ts">
import { ref } from 'vue'

const blurIntensity = ref(4)
</script>

<template>
  <svg class="svg_filter">
    <filter id="pixelate" x="0" y="0">
      <feFlood x="10" y="10" height="1" width="1" />
      <feComposite id="composite1" :width="blurIntensity" :height="blurIntensity" />
      <feTile result="a" />
      <feComposite in="SourceGraphic" in2="a" operator="in" />
      <feMorphology id="morphology" operator="dilate" :radius="blurIntensity / 2" />
    </filter>
  </svg>
  <v-slider
    class="slider"
    :elevation="7"
    v-model="blurIntensity"
    step="1"
    max="50"
    min="1"
  ></v-slider>
  <p>{{ blurIntensity }}</p>
</template>

<style scoped>
.slider {
  position: -webkit-sticky;
  position: sticky;
  top: 85vh;
  border: black double 3px;
  padding: 20px 10px 0px 10px;
  z-index: 999999;
  background-color: white;
}

.svg_filter {
  position: absolute;
}
</style>
