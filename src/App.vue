<template>
  <div class="dark-theme">
    <Navbar />
    <HeroSection id="home" />
    <VisionMission id="vision" />
    <Services id="services" />
    <Portfolio id="portfolio" />
    <Team id="team" />
    <Values id="values" />
    <Contact id="contact" />
    <footer class="bg-gray-800 text-center py-8 text-gray-300">
      <p>Welcome to Thousand Doors Studio</p>
    </footer>
  </div>
</template>

<script setup lang="ts">
import Navbar from './components/Navbar.vue'
import HeroSection from './components/HeroSection.vue'
import VisionMission from './components/VisionMission.vue'
import Services from './components/Services.vue'
import Portfolio from './components/Portfolio.vue'
import Team from './components/Team.vue'
import Values from './components/Values.vue'
import Contact from './components/Contact.vue'
</script>
