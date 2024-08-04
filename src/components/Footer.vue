<template>
    <footer class="bg-white py-6 text-center">
      <div class="container mx-auto">
        <div class="flex justify-center space-x-4 mb-4">
          <!-- Redes Sociais -->
          <a href="https://instagram.com/seuusuario" target="_blank" rel="noopener noreferrer" class="text-gray-600 hover:text-purple-600">
            <i class="fab fa-instagram fa-2x"></i>
          </a>
          <a href="https://facebook.com/seuusuario" target="_blank" rel="noopener noreferrer" class="text-gray-600 hover:text-purple-600">
            <i class="fab fa-facebook fa-2x"></i>
          </a>
        </div>
        <div class="text-xl font-semibold text-purple-600 mb-2">
          Vote 10
        </div>
        <div class="text-gray-500 text-sm">
          &copy; {{ new Date().getFullYear() }} - Criado por Garbson Souza
        </div>
      </div>
    </footer>
  </template>
  
  <script setup>
  // No additional script needed for this basic component
  </script>
  
  <style scoped>
  /* Import FontAwesome for social media icons */
  @import url('https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css');
  </style>
  