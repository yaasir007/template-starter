<template>
  <section id="contact" class="py-24 bg-white">
    <div class="mx-auto max-w-7xl px-4 sm:px-6 lg:px-8">
      <div class="grid grid-cols-1 gap-x-8 gap-y-10 lg:grid-cols-2">
        <!-- Contact Information -->
        <div>
          <h2 class="text-3xl font-bold tracking-tight text-gray-900">Contact Us</h2>
          <p class="mt-4 text-lg text-gray-600">
            Get in touch with us for all your plumbing needs. We're available 24/7 for emergencies.
          </p>

          <dl class="mt-8 space-y-6">
            <div class="flex gap-x-4">
              <dt class="flex-none">
                <span class="sr-only">Address</span>
                <MapPinIcon class="h-7 w-6 text-primary" />
              </dt>
              <dd>123 Plumbing Street<br>Anytown, ST 12345</dd>
            </div>
            <div class="flex gap-x-4">
              <dt class="flex-none">
                <span class="sr-only">Phone</span>
                <PhoneIcon class="h-7 w-6 text-primary" />
              </dt>
              <dd>
                <a class="hover:text-primary" href="tel:1234567890">(123) 456-7890</a>
              </dd>
            </div>
            <div class="flex gap-x-4">
              <dt class="flex-none">
                <span class="sr-only">Email</span>
                <EnvelopeIcon class="h-7 w-6 text-primary" />
              </dt>
              <dd>
                <a class="hover:text-primary" href="mailto:info@proplumbing.com">info@proplumbing.com</a>
              </dd>
            </div>
          </dl>
        </div>

        <!-- Contact Form -->
        <form class="flex flex-col gap-6">
          <div>
            <label for="name" class="block text-sm font-medium text-gray-700">Name</label>
            <input type="text" id="name" v-model="formData.name"
              class="mt-1 p-2 block w-full rounded-md border-gray-300 shadow-sm focus:border-primary focus:ring-primary">
          </div>
          <div>
            <label for="email" class="block text-sm font-medium text-gray-700">Email</label>
            <input type="email" id="email" v-model="formData.email"
              class="mt-1 p-2 block w-full rounded-md border-gray-300 shadow-sm focus:border-primary focus:ring-primary">
          </div>
          <div>
            <label for="message" class="block text-sm font-medium text-gray-700">Message</label>
            <textarea id="message" v-model="formData.message" rows="4"
              class="mt-1 p-2 block w-full rounded-md border-gray-300 shadow-sm focus:border-primary focus:ring-primary"></textarea>
          </div>
          <button type="submit" @click.prevent="submitForm"
            class="inline-flex justify-center rounded-md border border-transparent bg-primary px-4 py-2 text-sm font-medium text-white shadow-sm hover:bg-secondary focus:outline-none focus:ring-2 focus:ring-primary focus:ring-offset-2">
            Send Message
          </button>
        </form>
      </div>
    </div>
  </section>
</template>

<script setup lang="ts">
import { ref } from 'vue';
import { MapPinIcon, PhoneIcon, EnvelopeIcon } from '@heroicons/vue/24/outline';

const formData = ref({
  name: '',
  email: '',
  message: '',
});

const submitForm = () => {
  // Handle form submission here
  console.log('Form submitted:', formData.value);
  // Reset form
  formData.value = {
    name: '',
    email: '',
    message: '',
  };
};
</script>
