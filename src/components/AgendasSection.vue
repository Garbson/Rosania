<template>
  <section id="agendas" class="mb-12 p-6 bg-gray-100 rounded-lg shadow w-[90%] mx-auto">
    <h2 class="text-3xl font-semibold mb-4 text-black">🗓️ Pautas</h2>
    <div class="space-y-6">
      <div
        v-for="(agenda, index) in agendas"
        :key="index"
        class="p-4 bg-white rounded-lg shadow-md flex items-center space-x-4"
      >
        <div class="text-2xl">{{ agenda.icon }}</div>
        <div>
          <h3 class="text-xl font-semibold">{{ agenda.title }}</h3>
          <p class="text-lg">{{ agenda.description }}</p>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
const agendas = [
  {
    icon: "🌳",
    title: "Pauta 1: Preservação Ambiental",
    description:
      "Promoção de políticas para a preservação de áreas verdes na cidade.",
  },
  {
    icon: "🏫",
    title: "Pauta 2: Educação de Qualidade",
    description:
      "Melhorias no sistema educacional, com foco na capacitação de professores e infraestrutura escolar.",
  },
  {
    icon: "🏥",
    title: "Pauta 3: Saúde Pública",
    description:
      "Investimento em saúde pública, incluindo ampliação de postos de saúde e contratação de profissionais.",
  },
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
