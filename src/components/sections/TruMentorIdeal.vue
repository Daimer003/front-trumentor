<template>
    <section class="py-16 bg-white">
      <div class="container mx-auto px-4">
        <h2 class="text-3xl font-bold font-heading text-gray-800 text-center mb-12">
          TruMentor es Ideal Para Ti Si...
        </h2>
  
        <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-4 gap-8">
          <div
            v-for="(card, index) in cards"
            :key="index"
            class="bg-[var(--color-brand-50)] rounded-2xl p-8 transition-all duration-300 hover:shadow-modern hover:translate-y-[-5px] card-border"
          >
            <div class="bg-white w-14 h-14 rounded-full flex items-center justify-center shadow-md mb-6 text-[var(--color-brand-500)]">
              <i :class="`${card.icon} text-3xl`"></i>
            </div>
            <h3 class="text-xl font-semibold font-heading text-gray-800 mb-4">{{ card.title }}</h3>
            <p class="text-gray-600">{{ card.description }}</p>
          </div>
        </div>
      </div>
    </section>
  </template>
  
  <script setup>
  const cards = [
    {
      icon: 'bx bx-time-five',
      title: 'Te la pasas "apagando fuegos"',
      description:
        'Sientes que tu día a día se va en resolver urgencias, sin tiempo para pensar en el futuro de tu negocio o implementar mejoras reales que impulsen su crecimiento.',
    },
    {
      icon: 'bx bx-dollar-circle',
      title: 'Buscas crecer sin gastar fortunas',
      description:
        'Necesitas asesoría estratégica profesional, pero los consultores tradicionales están fuera de tu presupuesto como micro o pequeña empresa.',
    },
    {
      icon: 'bx bx-group',
      title: 'Tu equipo no está alineado',
      description:
        'Tus colaboradores no comparten la misma visión o no entienden hacia dónde va el negocio, generando descoordinación y duplicación de esfuerzos.',
    },
    {
      icon: 'bx bx-bar-chart-alt-2',
      title: 'Quieres decisiones basadas en datos',
      description:
        'Estás cansado de la improvisación y deseas un plan estructurado con objetivos claros y métricas de seguimiento para tu negocio.',
    },
  ];
  </script>
  