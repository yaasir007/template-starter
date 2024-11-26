<template>
  <section class="py-24 bg-white">
    <div class="mx-auto max-w-7xl px-4 sm:px-6 lg:px-8">
      <div class="text-center">
        <h2 class="text-3xl font-bold tracking-tight text-gray-900 sm:text-4xl">Why Choose Us</h2>
        <p class="mt-4 text-lg text-gray-600">Experience the difference with our professional plumbing services</p>
      </div>

      <div class="mt-16 grid grid-cols-1 gap-8 sm:grid-cols-2 lg:grid-cols-4">
        <div v-for="(feature, index) in features" :key="index" 
          class="flex flex-col items-center p-6 bg-gray-50 rounded-lg hover:shadow-lg transition-shadow">
          <div class="h-12 w-12 text-primary">
            <component :is="feature.icon" />
          </div>
          <h3 class="mt-4 text-lg font-semibold text-gray-900">{{ feature.title }}</h3>
          <p class="mt-2 text-center text-gray-600">{{ feature.description }}</p>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup lang="ts">
import { 
  ClockIcon, 
  ShieldCheckIcon, 
  CurrencyDollarIcon, 
  UserGroupIcon 
} from '@heroicons/vue/24/outline';

const features = [
  {
    title: '24/7 Service',
    description: 'Available around the clock for any plumbing emergency.',
    icon: ClockIcon,
  },
  {
    title: 'Licensed & Insured',
    description: 'Fully licensed professionals you can trust.',
    icon: ShieldCheckIcon,
  },
  {
    title: 'Fair Pricing',
    description: 'Competitive rates with no hidden fees.',
    icon: CurrencyDollarIcon,
  },
  {
    title: 'Expert Team',
    description: 'Experienced and certified plumbing professionals.',
    icon: UserGroupIcon,
  },
];
</script>