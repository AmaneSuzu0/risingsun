<script setup lang="ts">
defineProps<{
  title: string
  description: string
  icon: string
  color?: string
}>()
</script>

<template>
  <div 
    class="relative bg-white rounded-3xl shadow-lg p-6 transform hover:-translate-y-2 transition-all duration-300"
    :class="color || 'hover:shadow-primary/20'"
  >
    <div class="absolute -top-6 left-1/2 transform -translate-x-1/2">
      <div class="text-4xl floating">{{ icon }}</div>
    </div>
    <div class="mt-8 text-center">
      <h3 class="text-xl font-bold text-gray-900 mb-3">{{ title }}</h3>
      <p class="text-gray-600">{{ description }}</p>
    </div>
    <div class="absolute -bottom-3 right-3 text-3xl wiggle opacity-50">✨</div>
  </div>
</template>