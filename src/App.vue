<script setup lang="ts">
import TheHeader from './components/TheHeader.vue'
import HeroSection from './components/HeroSection.vue'
import WhyChooseUs from './components/WhyChooseUs.vue'
import ServicesSection from './components/ServicesSection.vue'
import TestimonialsSection from './components/TestimonialsSection.vue'
import ContactSection from './components/ContactSection.vue'
import TheFooter from './components/TheFooter.vue'
</script>

<template>
  <div class="min-h-screen">
    <TheHeader />
    <main>
      <HeroSection />
      <WhyChooseUs />
      <ServicesSection />
      <TestimonialsSection />
      <ContactSection />
    </main>
    <TheFooter />
  </div>
</template>