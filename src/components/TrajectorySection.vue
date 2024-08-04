<template>
    <section id="trajectory" class="mb-12 p-6 bg-gray-100 rounded-lg shadow w-[90%] mx-auto">
      <h2 class="text-3xl font-semibold mb-4 text-black">📚 Trajetória</h2>
      <div class="relative pl-8">
        <!-- Timeline Line -->
        <div class="absolute h-full border-l-2 border-purple-500 left-4 top-0"></div>
        <!-- Timeline Items -->
        <div v-for="(item, index) in items" :key="index" class="mb-8 flex items-center">
          <div class="w-8 h-8 bg-purple-500 rounded-full flex items-center justify-center text-white">{{ index + 1 }}</div>
          <div class="ml-4">
            <h3 class="text-xl font-semibold">{{ item.title }}</h3>
            <p class="text-lg">{{ item.description }}</p>
          </div>
        </div>
      </div>
    </section>
  </template>
  
  <script setup>
  const items = [
    { 
      title: 'Estudo na Escola Rui Barbosa', 
      description: 'Iniciou seus estudos na Escola Rui Barbosa, onde desenvolveu uma base sólida em várias disciplinas e participou ativamente de projetos extracurriculares.' 
    },
    { 
      title: 'Formação em Direito', 
      description: 'Concluiu o curso de Direito na Faculdade Exemplo, obtendo um conhecimento profundo em legislação e justiça, e se destacando como uma das melhores alunas da turma.' 
    },
    { 
      title: 'Experiência Profissional como Enfermeira', 
      description: 'Trabalhou como enfermeira no Hospital Saúde e Vida, onde atuou em diversas áreas, oferecendo cuidados essenciais aos pacientes e contribuindo para a melhoria dos processos hospitalares.' 
    }
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
  