<script setup lang="ts">
const contactDetails = [
  {
    icon: 'MapPinIcon',
    title: 'Visit Us',
    details: [
      'Rising Sun—Childhood Education Center',
      'Nanshan District',
      'Shenzhen, Guangdong Province',
      'China'
    ]
  },
  {
    icon: 'PhoneIcon',
    title: 'Contact',
    details: [
      'Phone: +86 755 1234 5678',
      'Email: info@risingsun-childhood.com',
      'WeChat: RisingSunEdu'
    ]
  },
  {
    icon: 'ClockIcon',
    title: 'Business Hours',
    details: [
      'Monday - Friday: 9:00 AM - 6:00 PM',
      'Saturday: 9:00 AM - 1:00 PM',
      'Sunday: Closed'
    ]
  }
]
</script>

<template>
  <div class="bg-white rounded-lg shadow-lg p-8">
    <div class="space-y-8">
      <div v-for="item in contactDetails" :key="item.title" class="flex space-x-4">
        <div class="flex-shrink-0">
          <component
            :is="item.icon"
            class="h-6 w-6 text-primary"
          />
        </div>
        <div>
          <h3 class="text-lg font-medium text-gray-900">{{ item.title }}</h3>
          <div class="mt-2 space-y-1">
            <p v-for="detail in item.details" :key="detail" class="text-gray-600">
              {{ detail }}
            </p>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>