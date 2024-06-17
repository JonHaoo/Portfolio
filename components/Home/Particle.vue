<template>
  <div ref="tsparticles"></div>
</template>

<script setup>
import { onMounted } from "vue";
import { loadStarsPreset } from "@tsparticles/preset-stars";

const tsparticles = ref(null);
onMounted(async () => {
  await loadStarsPreset(tsParticles);
  await tsParticles.load({
    id: "tsparticles",
    options: {
      preset: "stars",
    },
  });
});
</script>

<style scoped></style>
