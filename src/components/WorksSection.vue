<template>
    <section id="works" class="mb-12 p-6 bg-gray-100 rounded-lg shadow w-[90%] mx-auto">
      <h2 class="text-3xl font-semibold mb-4 text-black">💼 Conquistas</h2>
      <div class="space-y-6">
        <div v-for="(achievement, index) in achievements" :key="index" class="p-4 bg-white rounded-lg shadow-md flex items-center space-x-4">
          <div class="text-2xl">{{ achievement.icon }}</div>
          <div>
            <h3 class="text-xl font-semibold">{{ achievement.title }}</h3>
            <p class="text-lg">{{ achievement.description }}</p>
          </div>
        </div>
      </div>
    </section>
  </template>
  
  <script setup>
  const achievements = [
    { icon: '🏆', title: 'Melhoria na Saúde Comunitária', description: 'Implementação de novos programas de saúde, reduzindo doenças comuns em 30%.' },
    { icon: '🎓', title: 'Aumento na Qualidade da Educação', description: 'Criação de bolsas de estudo para alunos de baixa renda e reforma de escolas.' },
    { icon: '🚧', title: 'Infraestrutura Urbana', description: 'Revitalização de praças e ruas, promovendo um ambiente urbano mais seguro e agradável.' },
    { icon: '🌍', title: 'Projetos Ambientais Sustentáveis', description: 'Implementação de políticas ecológicas, como a plantação de árvores e campanhas de reciclagem.' },
    { icon: '🤝', title: 'Parcerias Comunitárias', description: 'Criação de parcerias com ONGs e empresas locais para apoiar projetos sociais e culturais.' }
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