<script setup lang="ts">
function toggleFullscreen() {
  const doc = document.documentElement;
  if (!document.fullscreenElement) {
    doc.requestFullscreen().catch((err) => {
      console.error(`Error attempting to enable full-screen mode: ${err.message}`);
    });
  } else {
    document.exitFullscreen();
  }
}
</script>

<template>
  <UButton
    icon="i-lucide-expand"
    class="absolute right-4 top-4 z-10"
    variant="outline"
    color="neutral"
    @click="toggleFullscreen"
  />
</template>
