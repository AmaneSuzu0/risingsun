<script setup lang="ts">
const navItems = [
  { name: 'Home', path: '/' },
  { name: 'About', path: '/about' },
  { name: 'Programs', path: '/programs' },
  { name: 'Contact', path: '/contact' }
]
</script>

<template>
  <nav class="bg-white shadow-lg">
    <div class="max-w-7xl mx-auto px-4">
      <div class="flex justify-between h-16">
        <div class="flex items-center">
          <router-link to="/" class="flex-shrink-0 flex items-center">
            <img class="h-12 w-auto" src="/images/logo.png" alt="Rising Sun Childhood" />
            <span class="ml-2 text-xl font-bold text-primary">Rising Sun—Childhood</span>
          </router-link>
        </div>
        <div class="flex items-center">
          <div class="hidden md:ml-6 md:flex md:space-x-8">
            <router-link
              v-for="item in navItems"
              :key="item.name"
              :to="item.path"
              class="text-gray-700 hover:text-primary px-3 py-2 rounded-md text-sm font-medium"
            >
              {{ item.name }}
            </router-link>
          </div>
        </div>
      </div>
    </div>
  </nav>
</template>