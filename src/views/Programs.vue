<script setup lang="ts">
import SectionHeader from '../components/SectionHeader.vue'

const programs = [
  {
    title: 'Financial Basics',
    duration: '8 weeks',
    ageGroup: '8-10 years',
    description: 'Introduction to money concepts, saving, and basic budgeting through interactive games and activities.',
    topics: ['Understanding Money', 'Saving Habits', 'Basic Budgeting', 'Smart Spending'],
    color: 'from-blue-500 to-blue-600'
  },
  {
    title: 'Young Entrepreneur',
    duration: '10 weeks',
    ageGroup: '10-12 years',
    description: 'Advanced program teaching entrepreneurship, project management, and team collaboration.',
    topics: ['Business Basics', 'Team Leadership', 'Project Planning', 'Market Understanding'],
    color: 'from-green-500 to-green-600'
  },
  {
    title: 'Money Masters',
    duration: '12 weeks',
    ageGroup: '11-12 years',
    description: 'Comprehensive financial education covering advanced topics and real-world applications.',
    topics: ['Investment Basics', 'Financial Planning', 'Digital Money', 'Economic Concepts'],
    color: 'from-purple-500 to-purple-600'
  }
]
</script>

<template>
  <div class="py-24 bg-gray-50">
    <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
      <SectionHeader
        title="Our Programs"
        subtitle="Comprehensive financial education programs tailored for young minds"
      />

      <div class="mt-16 grid gap-8 md:grid-cols-2 lg:grid-cols-3">
        <div
          v-for="program in programs"
          :key="program.title"
          class="bg-white rounded-xl shadow-lg overflow-hidden transform hover:-translate-y-1 transition-all duration-300"
        >
          <div :class="['bg-gradient-to-r', program.color, 'h-2']"></div>
          <div class="p-8">
            <h3 class="text-2xl font-bold text-gray-900 mb-4">{{ program.title }}</h3>
            <div class="flex space-x-4 text-sm text-gray-500 mb-6">
              <span class="flex items-center">
                <svg class="w-4 h-4 mr-2" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                  <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M12 8v4l3 3m6-3a9 9 0 11-18 0 9 9 0 0118 0z" />
                </svg>
                {{ program.duration }}
              </span>
              <span>|</span>
              <span class="flex items-center">
                <svg class="w-4 h-4 mr-2" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                  <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M17 20h5v-2a3 3 0 00-5.356-1.857M17 20H7m10 0v-2c0-.656-.126-1.283-.356-1.857M7 20H2v-2a3 3 0 015.356-1.857M7 20v-2c0-.656.126-1.283.356-1.857m0 0a5.002 5.002 0 019.288 0M15 7a3 3 0 11-6 0 3 3 0 016 0zm6 3a2 2 0 11-4 0 2 2 0 014 0zM7 10a2 2 0 11-4 0 2 2 0 014 0z" />
                </svg>
                {{ program.ageGroup }}
              </span>
            </div>
            <p class="text-gray-600 mb-6">{{ program.description }}</p>
            <div class="space-y-4">
              <h4 class="font-medium text-gray-900">Key Topics:</h4>
              <ul class="space-y-2">
                <li 
                  v-for="topic in program.topics" 
                  :key="topic"
                  class="flex items-center text-gray-600"
                >
                  <svg class="w-5 h-5 mr-2 text-green-500" fill="currentColor" viewBox="0 0 20 20">
                    <path fill-rule="evenodd" d="M10 18a8 8 0 100-16 8 8 0 000 16zm3.707-9.293a1 1 0 00-1.414-1.414L9 10.586 7.707 9.293a1 1 0 00-1.414 1.414l2 2a1 1 0 001.414 0l4-4z" clip-rule="evenodd" />
                  </svg>
                  {{ topic }}
                </li>
              </ul>
            </div>
          </div>
          <div class="px-8 py-6 bg-gray-50">
            <button class="w-full bg-primary text-white py-3 px-6 rounded-lg font-medium hover:bg-opacity-90 transition-colors duration-300 transform hover:-translate-y-0.5">
              Enroll Now
            </button>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>