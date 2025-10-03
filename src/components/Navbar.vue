<template>
  <nav class="bg-gray-900 text-white p-4 sticky top-0 z-50 shadow-lg">
    <div class="container mx-auto flex justify-between items-center relative">
      <div class="flex items-center">
        <img src="/logo.jpeg" alt="Thousand Doors Logo" class="h-10 w-10 mr-4 rounded-full" />
        <span class="text-xl font-bold text-orange-500">Thousand Doors</span>
      </div>
      <!-- Desktop Menu -->
      <ul class="hidden md:flex space-x-6">
        <li><a href="#home" class="hover:text-orange-500 transition">Home</a></li>
        <li><a href="#services" class="hover:text-orange-500 transition">Services</a></li>
        <li><a href="#portfolio" class="hover:text-orange-500 transition">Portfolio</a></li>
        <!-- <li><a href="#team" class="hover:text-orange-500 transition">Team</a></li> -->
        <li><a href="#values" class="hover:text-orange-500 transition">Values</a></li>
        <li><a href="#contact" class="hover:text-orange-500 transition">Contact</a></li>
      </ul>
      <!-- Mobile Burger Button -->
      <button
        @click="isMenuOpen = !isMenuOpen"
        class="md:hidden flex flex-col justify-center items-center space-y-1 p-2"
      >
        <span
          class="w-6 h-0.5 bg-white transition-transform"
          :class="{ 'rotate-45 translate-y-1.5': isMenuOpen }"
        ></span>
        <span
          class="w-6 h-0.5 bg-white transition-opacity"
          :class="{ 'opacity-0': isMenuOpen }"
        ></span>
        <span
          class="w-6 h-0.5 bg-white transition-transform"
          :class="{ '-rotate-45 -translate-y-1.5': isMenuOpen }"
        ></span>
      </button>
      <!-- Mobile Menu -->
      <div
        v-if="isMenuOpen"
        class="md:hidden absolute top-full left-0 w-full bg-gray-900 shadow-lg"
      >
        <ul class="flex flex-col space-y-4 p-4">
          <li>
            <a
              href="#home"
              @click="isMenuOpen = false"
              class="hover:text-orange-500 transition block py-2"
              >Home</a
            >
          </li>
          <li>
            <a
              href="#services"
              @click="isMenuOpen = false"
              class="hover:text-orange-500 transition block py-2"
              >Services</a
            >
          </li>
          <li>
            <a
              href="#portfolio"
              @click="isMenuOpen = false"
              class="hover:text-orange-500 transition block py-2"
              >Portfolio</a
            >
          </li>
          <li>
            <a
              href="#team"
              @click="isMenuOpen = false"
              class="hover:text-orange-500 transition block py-2"
              >Team</a
            >
          </li>
          <li>
            <a
              href="#values"
              @click="isMenuOpen = false"
              class="hover:text-orange-500 transition block py-2"
              >Values</a
            >
          </li>
          <li>
            <a
              href="#contact"
              @click="isMenuOpen = false"
              class="hover:text-orange-500 transition block py-2"
              >Contact</a
            >
          </li>
        </ul>
      </div>
    </div>
  </nav>
</template>

<script setup lang="ts">
import { ref } from 'vue'
const isMenuOpen = ref(false)
</script>
