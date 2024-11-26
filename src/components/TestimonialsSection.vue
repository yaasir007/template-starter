<template>
  <section id="testimonials" class="py-24 bg-gray-50">
    <div class="mx-auto max-w-7xl px-4 sm:px-6 lg:px-8">
      <div class="text-center">
        <h2 class="text-3xl font-bold tracking-tight text-gray-900 sm:text-4xl">
          What Our Customers Say
        </h2>
        <p class="mt-4 text-lg text-gray-600">
          Don't just take our word for it - hear from our satisfied customers
        </p>
      </div>

      <div class="mt-16 grid grid-cols-1 gap-8 sm:grid-cols-2 lg:grid-cols-3">
        <div v-for="(testimonial, index) in testimonials" :key="index"
          class="bg-white p-6 rounded-lg shadow-md hover:shadow-lg transition-shadow">
          <div class="flex items-center mb-4">
            <div class="flex-shrink-0">
              <img :src="testimonial.image" :alt="testimonial.name" class="h-12 w-12 rounded-full">
            </div>
            <div class="ml-4">
              <h3 class="text-lg font-medium text-gray-900">{{ testimonial.name }}</h3>
              <p class="text-gray-500">{{ testimonial.location }}</p>
            </div>
          </div>
          <p class="text-gray-600">{{ testimonial.text }}</p>
          <div class="mt-4 flex text-primary">
            <StarIcon v-for="star in 5" :key="star" class="h-5 w-5" />
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup lang="ts">
import { StarIcon } from '@heroicons/vue/24/solid';

const testimonials = [
  {
    name: 'John Smith',
    location: 'Local Homeowner',
    text: 'Excellent service! They responded quickly to my emergency call and fixed the issue professionally. The technician was knowledgeable and courteous.',
    image: 'https://randomuser.me/api/portraits/men/1.jpg',
  },
  {
    name: 'Sarah Johnson',
    location: 'Business Owner',
    text: "Very reliable and professional. They've been maintaining our commercial property for years. Always prompt and thorough with their work.",
    image: 'https://randomuser.me/api/portraits/women/2.jpg',
  },
  {
    name: 'Mike Wilson',
    location: 'Homeowner',
    text: 'Fair pricing and great workmanship. I highly recommend their services to everyone. They installed my new water heater quickly and efficiently.',
    image: 'https://randomuser.me/api/portraits/men/3.jpg',
  },
  {
    name: 'Emily Davis',
    location: 'Restaurant Owner',
    text: 'Their emergency service saved our business from a major plumbing disaster. The team was professional and worked quickly to resolve the issue.',
    image: 'https://randomuser.me/api/portraits/women/4.jpg',
  },
  {
    name: 'Robert Chen',
    location: 'Property Manager',
    text: 'We use their maintenance service for multiple properties. Always reliable, professional, and thorough with their work.',
    image: 'https://randomuser.me/api/portraits/men/5.jpg',
  },
  {
    name: 'Lisa Thompson',
    location: 'Homeowner',
    text: 'They did an amazing job with our bathroom remodel. The attention to detail and quality of work exceeded our expectations.',
    image: 'https://randomuser.me/api/portraits/women/6.jpg',
  },
];
</script>