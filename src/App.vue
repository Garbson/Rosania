<template>
  <div class="min-h-screen bg-gradient-to-br from-purple-600 to-pink-500">
    <Header />
    <main class="container mx-auto mt-12">
      <TrajectorySection />
      <WorksSection />
      <AgendasSection />
      <OpinionsSection />
    </main>
    <Footer />
  </div>
</template>

<script setup>
import Header from './components/Header.vue';
import TrajectorySection from './components/TrajectorySection.vue';
import WorksSection from './components/WorksSection.vue';
import AgendasSection from './components/AgendasSection.vue';
import OpinionsSection from './components/OpinionsSection.vue';
import Footer from './components/Footer.vue';
</script>
