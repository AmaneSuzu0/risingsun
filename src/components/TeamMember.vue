<script setup lang="ts">
defineProps<{
  name: string
  role: string
  bio: string
  image: string
  socialLinks?: {
    type: string
    url: string
  }[]
}>()
</script>

<template>
  <div class="bg-white rounded-xl shadow-lg p-6 transform hover:-translate-y-1 transition-all duration-300">
    <div class="text-center">
      <div class="relative w-40 h-40 mx-auto mb-4">
        <div class="absolute inset-0 bg-gradient-to-br from-primary to-secondary rounded-full opacity-20 animate-pulse"></div>
        <img 
          :src="image" 
          :alt="name" 
          class="rounded-full object-cover w-full h-full relative z-10 border-4 border-white shadow-lg"
        />
        <div class="absolute -bottom-2 -right-2 text-3xl floating">✨</div>
      </div>
      <h3 class="text-xl font-bold text-gray-900 mb-2">{{ name }}</h3>
      <p class="text-primary font-medium mb-4">{{ role }}</p>
      <p class="text-gray-600 text-sm mb-4">{{ bio }}</p>
      <div v-if="socialLinks" class="flex justify-center space-x-4">
        <a 
          v-for="link in socialLinks" 
          :key="link.type"
          :href="link.url"
          target="_blank"
          rel="noopener noreferrer"
          class="text-gray-400 hover:text-primary transition-colors"
        >
          <component :is="link.type" class="h-5 w-5" />
        </a>
      </div>
    </div>
  </div>
</template>