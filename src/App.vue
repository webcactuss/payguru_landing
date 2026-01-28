<script setup lang="ts">
import Hero from "@/sections/Hero.vue";
import Header from "@/components/Header.vue";
import Logos from "@/sections/Logos.vue";
import TechSupport from "@/sections/TechSupport.vue";
import ContactUs from "@/components/ContactUs.vue";
import Footer from "@/sections/Footer.vue";
import TechnologiesInProcess from "@/sections/TechnologiesInProcess.vue";
import WhiteLabel from "@/sections/WhiteLabel.vue";
import FastStart from "@/sections/FastStart.vue";
import Features from "@/sections/Features.vue";
import Geography from "@/sections/Geography.vue";
</script>

<template>
  <Header />
  <main>
    <Hero />
    <Logos />
    <Geography />
    <TechnologiesInProcess />
    <Features />
    <WhiteLabel />
    <FastStart />
    <TechSupport />
    <ContactUs />
    <Footer />
  </main>
</template>

<style scoped>
</style>
