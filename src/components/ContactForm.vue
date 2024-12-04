<script setup lang="ts">
import { ref } from 'vue'

const form = ref({
  name: '',
  email: '',
  phone: '',
  subject: '',
  message: ''
})

const handleSubmit = (e: Event) => {
  e.preventDefault()
  // Form submission logic would go here
  console.log('Form submitted:', form.value)
}
</script>

<template>
  <form @submit="handleSubmit" class="bg-white rounded-lg shadow-lg p-8 space-y-6">
    <div class="grid grid-cols-1 gap-6 sm:grid-cols-2">
      <div>
        <label for="name" class="block text-sm font-medium text-gray-700">Full Name</label>
        <input
          type="text"
          id="name"
          v-model="form.name"
          class="mt-1 block w-full rounded-md border-gray-300 shadow-sm focus:border-primary focus:ring-primary"
          required
        />
      </div>

      <div>
        <label for="email" class="block text-sm font-medium text-gray-700">Email</label>
        <input
          type="email"
          id="email"
          v-model="form.email"
          class="mt-1 block w-full rounded-md border-gray-300 shadow-sm focus:border-primary focus:ring-primary"
          required
        />
      </div>
    </div>

    <div class="grid grid-cols-1 gap-6 sm:grid-cols-2">
      <div>
        <label for="phone" class="block text-sm font-medium text-gray-700">Phone Number</label>
        <input
          type="tel"
          id="phone"
          v-model="form.phone"
          class="mt-1 block w-full rounded-md border-gray-300 shadow-sm focus:border-primary focus:ring-primary"
        />
      </div>

      <div>
        <label for="subject" class="block text-sm font-medium text-gray-700">Subject</label>
        <input
          type="text"
          id="subject"
          v-model="form.subject"
          class="mt-1 block w-full rounded-md border-gray-300 shadow-sm focus:border-primary focus:ring-primary"
          required
        />
      </div>
    </div>

    <div>
      <label for="message" class="block text-sm font-medium text-gray-700">Message</label>
      <textarea
        id="message"
        v-model="form.message"
        rows="4"
        class="mt-1 block w-full rounded-md border-gray-300 shadow-sm focus:border-primary focus:ring-primary"
        required
      ></textarea>
    </div>

    <button
      type="submit"
      class="w-full bg-primary text-white py-3 px-6 rounded-md hover:bg-opacity-90 transition-colors duration-300 transform hover:-translate-y-0.5"
    >
      Send Message
    </button>
  </form>
</template>