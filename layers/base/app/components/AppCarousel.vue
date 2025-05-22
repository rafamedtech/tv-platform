<script setup lang="ts">
const items = [
  'https://res.cloudinary.com/rafamed-dev/image/upload/v1747952441/Screenshot_2025-05-22_at_3.20.31_p.m._uk1lm5.png',
  'https://res.cloudinary.com/rafamed-dev/image/upload/v1747950729/tv_dv3rnt.jpg',
  'https://res.cloudinary.com/rafamed-dev/image/upload/v1747952441/Screenshot_2025-05-22_at_3.20.31_p.m._uk1lm5.png',
  'https://res.cloudinary.com/rafamed-dev/image/upload/v1747950729/tv_dv3rnt.jpg',
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
