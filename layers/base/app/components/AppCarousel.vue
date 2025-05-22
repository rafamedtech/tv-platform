<script setup lang="ts">
const items = [
  'https://res.cloudinary.com/rafamed-dev/image/upload/v1747954693/olivoweb_amkcv5.jpg',
  'https://res.cloudinary.com/rafamed-dev/image/upload/v1747954693/oivoweb2_rdgzei.jpg',
  'https://res.cloudinary.com/rafamed-dev/image/upload/v1747954693/OLIVOWEB3_akia1i.jpg',
];
</script>

<template>
  <section class="min-h-dvh h-dvh flex items-center justify-center w-dvh">
    <UCarousel
      v-slot="{ item }"
      loop
      :autoplay="{ delay: 5000 }"
      :items="items"
      :ui="{ item: 'basis-[100%]', root: 'h-full' }"
    >
      <img :src="item" class="rounded-lg h-screen object-cover" />
    </UCarousel>
  </section>
</template>
