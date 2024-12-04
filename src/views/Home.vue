<script setup lang="ts">
import { ref } from 'vue'
import ChildFriendlyCard from '../components/ChildFriendlyCard.vue'

const benefits = [
  {
    title: 'Money Adventures',
    description: 'Join our fun journey to learn about money and savings!',
    icon: '🎮'
  },
  {
    title: 'Grow Together',
    description: 'Make new friends while learning valuable life skills',
    icon: '🌱'
  },
  {
    title: 'Fun Challenges',
    description: 'Complete exciting missions and earn rewards',
    icon: '🎯'
  }
]

const stats = [
  { number: '1000+', label: 'Happy Students', icon: '😊' },
  { number: '95%', label: 'Fun Learning', icon: '🌟' },
  { number: '3', label: 'Amazing Programs', icon: '🎨' }
]

const mascotTips = [
  "Remember to save some pocket money! 💰",
  "Learning about money is fun! 🎮",
  "Share what you learn with friends! 🤝"
]

const currentTip = ref(0)

const changeTip = () => {
  currentTip.value = (currentTip.value + 1) % mascotTips.length
}
</script>

<template>
  <div class="min-h-screen">
    <!-- Hero Section -->
    <div class="relative bg-gradient-to-r from-primary to-secondary py-32 overflow-hidden">
      <div class="absolute inset-0 bg-pattern opacity-10"></div>
      <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 relative">
        <div class="text-center">
          <div class="text-6xl mb-8 floating">🌅</div>
          <h1 class="text-4xl font-bold text-white sm:text-5xl md:text-6xl">
            Welcome to Rising Sun!<br />
            <span class="text-accent">Where Learning is Fun!</span>
          </h1>
          <p class="mt-6 max-w-md mx-auto text-xl text-white opacity-90 sm:max-w-3xl">
            Join our exciting journey to become money-smart! 🚀
          </p>
          <div class="mt-10 max-w-md mx-auto sm:flex sm:justify-center md:mt-12">
            <div class="rounded-md shadow">
              <router-link
                to="/programs"
                class="w-full flex items-center justify-center px-8 py-4 border border-transparent text-lg font-medium rounded-md text-primary bg-white hover:bg-gray-50 transition-colors duration-300"
              >
                Start Your Adventure! 🎉
              </router-link>
            </div>
          </div>
        </div>
      </div>
    </div>

    <!-- Mascot Tip Section -->
    <div class="relative -mt-16 mb-12">
      <div class="max-w-lg mx-auto px-4">
        <div 
          class="bubble bg-white shadow-lg text-center cursor-pointer"
          @click="changeTip"
        >
          <div class="text-4xl mb-2 bouncing">🦊</div>
          <p class="text-lg text-gray-700">{{ mascotTips[currentTip] }}</p>
        </div>
      </div>
    </div>

    <!-- Stats Section -->
    <div class="bg-white py-12">
      <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
        <div class="bg-white rounded-lg shadow-xl p-8">
          <div class="grid grid-cols-1 gap-8 sm:grid-cols-3">
            <div 
              v-for="stat in stats" 
              :key="stat.label"
              class="text-center"
            >
              <div class="text-4xl mb-2 bouncing">{{ stat.icon }}</div>
              <div class="text-4xl font-bold text-primary">{{ stat.number }}</div>
              <div class="mt-2 text-gray-600">{{ stat.label }}</div>
            </div>
          </div>
        </div>
      </div>
    </div>

    <!-- Benefits Section -->
    <div class="py-24 bg-gray-50">
      <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
        <div class="lg:text-center mb-24">
          <div class="text-5xl mb-4 floating">🌈</div>
          <h2 class="text-3xl font-bold text-gray-900 sm:text-4xl">
            Join Our Fun Learning Adventure!
          </h2>
          <p class="mt-4 max-w-2xl text-xl text-gray-500 lg:mx-auto">
            Discover the exciting world of money and friendship! ✨
          </p>
        </div>

        <div class="grid grid-cols-1 gap-16 sm:grid-cols-2 lg:grid-cols-3">
          <ChildFriendlyCard
            v-for="benefit in benefits"
            :key="benefit.title"
            v-bind="benefit"
          />
        </div>
      </div>
    </div>
  </div>
</template>

<style scoped>
.bg-pattern {
  background-image: url("data:image/svg+xml,%3Csvg width='60' height='60' viewBox='0 0 60 60' xmlns='http://www.w3.org/2000/svg'%3E%3Cg fill='none' fill-rule='evenodd'%3E%3Cg fill='%23ffffff' fill-opacity='0.4'%3E%3Cpath d='M36 34v-4h-2v4h-4v2h4v4h2v-4h4v-2h-4zm0-30V0h-2v4h-4v2h4v4h2V6h4V4h-4zM6 34v-4H4v4H0v2h4v4h2v-4h4v-2H6zM6 4V0H4v4H0v2h4v4h2V6h4V4H6z'/%3E%3C/g%3E%3C/g%3E%3C/svg%3E");
}
</style>