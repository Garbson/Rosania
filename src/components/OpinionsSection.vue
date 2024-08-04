<template>
    <section id="opinions" class="mb-12 p-6 bg-gray-100 rounded-lg shadow w-[90%] mx-auto">
      <h2 class="text-3xl font-semibold mb-4 text-black">🗣️ Opiniões</h2>
      <div class="space-y-6">
        <div v-for="(opinion, index) in opinions" :key="index" class="p-4 bg-white rounded-lg shadow-md flex items-center space-x-4">
          <img :src="opinion.img" alt="Pessoa" class="w-16 h-16 rounded-full object-cover">
          <div>
            <p class="font-semibold">{{ opinion.name }}:</p>
            <p class="text-lg">{{ opinion.text }}</p>
          </div>
        </div>
      </div>
    </section>
  </template>
  
  <script setup>
  const opinions = [
    { img: '/persona1.jpeg', name: 'João Silva', text: 'Trabalhei com Rosania na área da saúde. Ela é uma pessoa dedicada, que ama o próximo e busca ajudar a quem ela pode.' },
    { img: '/persona2.jpeg', name: 'Maria Oliveira', text: 'Rosania tem uma visão inovadora e sempre busca soluções práticas para os problemas da comunidade.' },
    { img: '/persona3.jpeg', name: 'Carlos Souza', text: 'Seu trabalho na educação é exemplar, sempre focada em melhorar a qualidade de ensino para todos.' },
    { img: '/persona4.jpeg', name: 'Ana Costa', text: 'Rosania é uma líder inspiradora, que demonstra um grande compromisso com o desenvolvimento da nossa cidade.' }
  ];
  </script>
  <style scoped>
  h1,
  h2 {
    color: #000000; /* Cor do texto preto para contraste */
  }
  
  section {
    transition: transform 0.3s, box-shadow 0.3s;
  }
  
  section:hover {
    transform: scale(1.02);
    box-shadow: 0 10px 20px rgba(0, 0, 0, 0.15);
  }
  </style>