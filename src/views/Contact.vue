<script setup lang="ts">
import SectionHeader from '../components/SectionHeader.vue'
import ContactInfo from '../components/ContactInfo.vue'
import ContactForm from '../components/ContactForm.vue'
import { MapPinIcon, PhoneIcon, ClockIcon } from '@heroicons/vue/24/outline'
</script>

<template>
  <div class="py-12 bg-gray-50">
    <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
      <SectionHeader
        title="Contact Us"
        subtitle="Get in touch with our team to learn more about our programs"
      />

      <div class="mt-12 grid grid-cols-1 gap-8 lg:grid-cols-2">
        <ContactInfo />
        <ContactForm />
      </div>

      <!-- Map Section -->
      <div class="mt-16">
        <div class="bg-white rounded-lg shadow-lg overflow-hidden">
          <iframe
            src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d3691.9901!2d114.0545!3d22.5445!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x0%3A0x0!2zMjLCsDMyJzQwLjIiTiAxMTTCsDAzJzE2LjIiRQ!5e0!3m2!1sen!2sus!4v1234567890"
            width="100%"
            height="400"
            style="border:0;"
            allowfullscreen=""
            loading="lazy"
            referrerpolicy="no-referrer-when-downgrade"
          ></iframe>
        </div>
      </div>
    </div>
  </div>
</template>