<template>
  <footer class="bg-gray-900">
    <div class="mx-auto max-w-7xl px-4 py-12 sm:px-6 lg:px-8">
      <div class="grid grid-cols-1 md:grid-cols-3 gap-8">
        <!-- Company Info -->
        <div>
          <h3 class="text-white text-lg font-semibold mb-4">Pro Plumbing</h3>
          <p class="text-gray-400">Professional plumbing services you can trust. Available 24/7 for all your plumbing needs.</p>
        </div>

        <!-- Quick Links -->
        <div>
          <h3 class="text-white text-lg font-semibold mb-4">Quick Links</h3>
          <ul class="space-y-2">
            <li><a href="#" class="text-gray-400 hover:text-white">Home</a></li>
            <li><a href="#services" class="text-gray-400 hover:text-white">Services</a></li>
            <li><a href="#testimonials" class="text-gray-400 hover:text-white">Testimonials</a></li>
            <li><a href="#contact" class="text-gray-400 hover:text-white">Contact</a></li>
          </ul>
        </div>

        <!-- Contact Info -->
        <div>
          <h3 class="text-white text-lg font-semibold mb-4">Contact Us</h3>
          <ul class="space-y-2 text-gray-400">
            <li>123 Plumbing Street</li>
            <li>Anytown, ST 12345</li>
            <li><a href="tel:1234567890" class="hover:text-white">(123) 456-7890</a></li>
            <li><a href="mailto:info@proplumbing.com" class="hover:text-white">info@proplumbing.com</a></li>
          </ul>
        </div>
      </div>

      <div class="mt-8 pt-8 border-t border-gray-800 text-center text-gray-400">
        <p>&copy; {{ new Date().getFullYear() }} Pro Plumbing. All rights reserved.</p>
      </div>
    </div>
  </footer>
</template>