<script setup lang="ts">
import { ref } from 'vue';
import { Bars3Icon, XMarkIcon } from '@heroicons/vue/24/outline';

const isMenuOpen = ref(false);

const navigation = [
  { name: 'Home', href: '#' },
  { name: 'Services', href: '#services' },
  { name: 'Testimonials', href: '#testimonials' },
  { name: 'Contact', href: '#contact' },
];
</script>

<template>
  <header class="bg-white shadow-md fixed w-full top-0 z-50">
    <nav class="mx-auto max-w-7xl px-4 sm:px-6 lg:px-8">
      <div class="flex h-16 justify-between">
        <div class="flex">
          <div class="flex flex-shrink-0 items-center">
            <h1 class="text-2xl font-bold text-primary">Pro Plumbing</h1>
          </div>
        </div>
        
        <!-- Desktop menu -->
        <div class="hidden sm:flex sm:items-center">
          <div class="flex space-x-4">
            <a v-for="item in navigation" :key="item.name" :href="item.href"
              class="px-3 py-2 text-sm font-medium text-gray-700 hover:text-primary">
              {{ item.name }}
            </a>
          </div>
          <a href="tel:1234567890" 
            class="ml-8 inline-flex items-center px-4 py-2 border border-transparent text-sm font-medium rounded-md text-white bg-primary hover:bg-secondary">
            Call Now: (123) 456-7890
          </a>
        </div>

        <!-- Mobile menu button -->
        <div class="flex items-center sm:hidden">
          <button @click="isMenuOpen = !isMenuOpen" class="p-2 text-gray-600">
            <Bars3Icon v-if="!isMenuOpen" class="h-6 w-6" />
            <XMarkIcon v-else class="h-6 w-6" />
          </button>
        </div>
      </div>

      <!-- Mobile menu -->
      <div v-show="isMenuOpen" class="sm:hidden">
        <div class="space-y-1 pb-3 pt-2">
          <a v-for="item in navigation" :key="item.name" :href="item.href"
            class="block px-3 py-2 text-base font-medium text-gray-700 hover:text-primary"
            @click="isMenuOpen = false">
            {{ item.name }}
          </a>
          <a href="tel:1234567890" 
            class="block px-3 py-2 text-base font-medium text-primary hover:text-secondary">
            Call Now: (123) 456-7890
          </a>
        </div>
      </div>
    </nav>
  </header>
</template>