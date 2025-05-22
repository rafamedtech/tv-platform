<script setup lang="ts">
const items = [
  'https://res.cloudinary.com/rafamed-dev/image/upload/v1747954693/olivoweb_amkcv5.jpg',
  'https://res.cloudinary.com/rafamed-dev/image/upload/v1747954693/oivoweb2_rdgzei.jpg',
  'https://res.cloudinary.com/rafamed-dev/image/upload/v1747954693/OLIVOWEB3_akia1i.jpg',
];
</script>

<template>
  <section class="flex items-center justify-center">
    <!-- <FullscreenButton /> -->
    <UCarousel v-slot="{ item }" loop :autoplay="{ delay: 5000 }" :items="items">
      <img :src="item" />
    </UCarousel>
  </section>
</template>
