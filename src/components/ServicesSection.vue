<template>
  <section id="services" class="py-24 bg-white">
    <div class="mx-auto max-w-7xl px-4 sm:px-6 lg:px-8">
      <div class="text-center">
        <h2 class="text-3xl font-bold tracking-tight text-gray-900 sm:text-4xl">Our Services</h2>
        <p class="mt-4 text-lg text-gray-600">Comprehensive plumbing solutions for your home and business</p>
      </div>

      <div class="mt-16 grid grid-cols-1 gap-8 sm:grid-cols-2 lg:grid-cols-3">
        <div v-for="(service, index) in services" :key="index" 
          class="flex flex-col items-center p-6 bg-gray-50 rounded-lg hover:shadow-lg transition-shadow">
          <div class="h-16 w-16 text-primary">
            <component :is="service.icon" />
          </div>
          <h3 class="mt-4 text-xl font-semibold text-gray-900">{{ service.title }}</h3>
          <p class="mt-2 text-center text-gray-600">{{ service.description }}</p>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup lang="ts">
import { 
  WrenchScrewdriverIcon, 
  FireIcon, 
  HomeIcon, 
  BuildingOfficeIcon,
  HomeModernIcon,
  WrenchIcon,
  BeakerIcon,
  SparklesIcon,
  ArrowPathIcon
} from '@heroicons/vue/24/outline';

const services = [
  {
    title: 'Emergency Repairs',
    description: '24/7 emergency plumbing services for when you need help right away.',
    icon: WrenchScrewdriverIcon,
  },
  {
    title: 'Water Heater Services',
    description: 'Installation, repair, and maintenance of all types of water heaters.',
    icon: FireIcon,
  },
  {
    title: 'Residential Plumbing',
    description: 'Complete home plumbing services from repairs to new installations.',
    icon: HomeIcon,
  },
  {
    title: 'Commercial Services',
    description: 'Specialized plumbing solutions for businesses and commercial properties.',
    icon: BuildingOfficeIcon,
  },
  {
    title: 'Bathroom Remodeling',
    description: 'Expert bathroom renovation and fixture installation services.',
    icon: HomeModernIcon,
  },
  {
    title: 'Pipe Repairs',
    description: 'Professional pipe repair, replacement, and maintenance services.',
    icon: WrenchIcon,
  },
  {
    title: 'Water Treatment',
    description: 'Water softening, filtration, and purification systems.',
    icon: BeakerIcon,
  },
  {
    title: 'Drain Cleaning',
    description: 'Professional drain cleaning and clog removal services.',
    icon: SparklesIcon,
  },
  {
    title: 'Maintenance Plans',
    description: 'Regular maintenance programs to prevent plumbing issues.',
    icon: ArrowPathIcon,
  },
];
</script>