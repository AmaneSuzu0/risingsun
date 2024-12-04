<script setup lang="ts">
defineProps<{
  title: string
  subtitle?: string
}>()
</script>

<template>
  <div class="lg:text-center mb-12">
    <h2 class="text-3xl font-bold text-gray-900">{{ title }}</h2>
    <p v-if="subtitle" class="mt-4 max-w-2xl text-xl text-gray-500 lg:mx-auto">
      {{ subtitle }}
    </p>
  </div>
</template>