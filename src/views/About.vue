<script setup lang="ts">
import SectionHeader from '../components/SectionHeader.vue'
import TeamMember from '../components/TeamMember.vue'

const team = [
  {
    name: 'Xiaohan (Jane) Li',
    role: 'Chief Operating Officer',
    image: '/images/team/jane.png',
    bio: 'Jane brings over 10 years of experience in education management. She is passionate about creating engaging learning experiences for children.',
    socialLinks: [
      { type: 'linkedin', url: 'https://linkedin.com/in/jane-li' },
      { type: 'twitter', url: 'https://twitter.com/jane_li' }
    ]
  },
  {
    name: 'Jiasheng (Eric) Ye',
    role: 'Chief Marketing Officer',
    image: '/images/team/eric.png',
    bio: 'Eric is a marketing expert with a focus on educational technology. He believes in making financial education fun and accessible for all children.',
    socialLinks: [
      { type: 'linkedin', url: 'https://linkedin.com/in/eric-ye' },
      { type: 'twitter', url: 'https://twitter.com/eric_ye' }
    ]
  },
  {
    name: 'Guoping (Owen) Li',
    role: 'Chief Executive Officer',
    image: '/images/team/owen.png',
    bio: 'Owen has dedicated his career to improving financial literacy among young people. He leads Rising Sun with a vision of empowering the next generation.',
    socialLinks: [
      { type: 'linkedin', url: 'https://linkedin.com/in/owen-li' },
      { type: 'twitter', url: 'https://twitter.com/owen_li' }
    ]
  }
]
</script>

<template>
  <div class="py-12 bg-gray-50">
    <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
      <SectionHeader
        title="About Rising Sun—Childhood"
        subtitle="Empowering the next generation with financial intelligence"
      />
      
      <div class="mt-10 prose prose-lg mx-auto">
        <p class="text-lg text-gray-600 leading-relaxed">
          Rising Sun—Childhood is dedicated to filling the gap in financial education in China,
          particularly in Shenzhen. We focus on children aged 8-12, providing them with essential
          financial knowledge and skills that will serve them throughout their lives.
        </p>
        
        <div class="my-12 bg-white rounded-xl p-8 shadow-lg">
          <h3 class="text-2xl font-bold text-primary mb-4">Our Vision</h3>
          <p class="text-gray-600">
            We envision a future where every child in Shenzhen has access to quality financial education,
            enabling them to make informed financial decisions and develop healthy money management habits
            from an early age.
          </p>
          <div class="mt-6 grid grid-cols-1 md:grid-cols-3 gap-6">
            <div class="text-center p-4">
              <div class="text-4xl mb-2 floating">🎯</div>
              <h4 class="font-bold text-gray-900">Mission-Driven</h4>
              <p class="text-sm text-gray-600">Dedicated to financial literacy</p>
            </div>
            <div class="text-center p-4">
              <div class="text-4xl mb-2 floating">🌱</div>
              <h4 class="font-bold text-gray-900">Child-Focused</h4>
              <p class="text-sm text-gray-600">Age-appropriate learning</p>
            </div>
            <div class="text-center p-4">
              <div class="text-4xl mb-2 floating">🤝</div>
              <h4 class="font-bold text-gray-900">Community-Based</h4>
              <p class="text-sm text-gray-600">Local impact, global thinking</p>
            </div>
          </div>
        </div>
      </div>

      <div class="mt-16">
        <h3 class="text-3xl font-bold text-center mb-2">Meet Our Team</h3>
        <p class="text-center text-gray-600 mb-12">The passionate educators behind Rising Sun—Childhood</p>
        <div class="grid grid-cols-1 gap-8 md:grid-cols-2 lg:grid-cols-3">
          <TeamMember
            v-for="member in team"
            :key="member.name"
            v-bind="member"
          />
        </div>
      </div>
    </div>
  </div>
</template>