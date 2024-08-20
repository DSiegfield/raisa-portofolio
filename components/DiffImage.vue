<script setup lang="ts">
const props = defineProps<{
  title: string;
  description: string;
  imageSrcAntes: string;
  imageSrcDepois: string;
}>();
</script>

<template>
  <h1 class="text-4xl lg:text-7xl mb-3">{{ title }}</h1>
  <h2 class="text-xl lg:text-2xl mb-3">{{ description }}</h2>
  <div class="diff aspect-[16/9]">
    <div class="diff-item-1">
      <NuxtImg alt="daisy" :src="imageSrcDepois" />
    </div>
    <div class="diff-item-2">
      <NuxtImg alt="daisy" :src="imageSrcAntes" />
    </div>
    <div class="diff-resizer"></div>
  </div>
</template>
