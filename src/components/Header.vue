<template>
    <header class="relative h-96">
      <img src="/rosania.jpg" alt="Vereadora Nome" class="w-full h-full object-cover object-top">
      <div class="absolute inset-0 bg-black opacity-50"></div>
      <nav class="absolute top-0 left-0 w-full p-6 flex justify-between items-center text-white">
        <!-- Menu Button -->
        <button @click="toggleMenu" class="text-3xl md:hidden">
          <span v-if="!isMenuOpen">☰</span> <!-- Menu emoji -->
          <span v-if="isMenuOpen" class="text-2xl">❌</span> <!-- Close emoji with reduced size -->
        </button>
  
        <!-- Desktop Menu -->
        <div class="flex items-center space-x-2 w-40 h-20 rounded-full hidden md:flex">
          <span class="text-3xl font-bold text-purple-600">Vote</span>
          <span class="text-5xl font-extrabold text-pink-500">10</span>
        </div>
        <ul class="flex space-x-6 text-lg hidden md:flex">
          <li><a href="#trajectory" class="hover:underline">📚 Trajetória</a></li>
          <li><a href="#works" class="hover:underline">💼 Conquistas</a></li>
          <li><a href="#agendas" class="hover:underline">🗓️ Pautas</a></li>
          <li><a href="#opinions" class="hover:underline">🗣️ Opiniões</a></li>
        </ul>
  
        <!-- Mobile Menu Sidebar -->
        <div v-if="isMenuOpen" class="fixed inset-0 bg-black bg-opacity-80 z-50 md:hidden">
          <div class="w-3/4 sm:w-1/2 md:w-1/3 bg-black bg-opacity-60 h-full p-6 relative">
            <button @click="toggleMenu" class="absolute  right-4 text-2xl text-white">
              ❌
            </button>
            <div class="flex items-center space-x-2 w-full h-20 mb-6 rounded-full">
              <span class="text-3xl font-bold text-purple-600">Vote</span>
              <span class="text-5xl font-extrabold text-pink-500">10</span>
            </div>
            <ul class="flex flex-col space-y-6 text-lg text-white">
              <li><a href="#trajectory" @click="toggleMenu" class="hover:underline">📚 Trajetória</a></li>
              <li><a href="#works" @click="toggleMenu" class="hover:underline">💼 Conquistas</a></li>
              <li><a href="#agendas" @click="toggleMenu" class="hover:underline">🗓️ Pautas</a></li>
              <li><a href="#opinions" @click="toggleMenu" class="hover:underline">🗣️ Opiniões</a></li>
            </ul>
          </div>
        </div>
      </nav>
    </header>
  </template>
  
  <script setup>
  import { ref } from 'vue';
  
  const isMenuOpen = ref(false);
  
  const toggleMenu = () => {
    isMenuOpen.value = !isMenuOpen.value;
  };
  </script>
  
  <style scoped>
  header img {
    width: 100%;
    height: 100%;
    object-fit: cover;
    object-position: top;
  }
  
  nav button {
    background: none;
    border: none;
    cursor: pointer;
  }
  </style>
  