<script setup>
import AppHeader from './components/AppHeader.vue';
import AppHero from './components/AppHero.vue';
import AboutSection from './components/AboutSection.vue';
import LearningSection from './components/LearningSection.vue';
import FormSection from './components/FormSection.vue';
import AppFooter from './components/AppFooter.vue';
</script>

<template>
  <AppHeader />
  <main>
    <AppHero />
    <AboutSection />
    <LearningSection />
    <FormSection />
  </main>
  <AppFooter />
</template>

<style scoped></style>
