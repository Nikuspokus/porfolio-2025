<template>
  <NPageHero
    title="Votre solution SaaS complète"
    description="Créez, gérez et développez votre entreprise avec une solution intuitive et performante."
    :primaryAction="{ label: 'Commencer maintenant', link: '/inscription' }"
    :secondaryAction="{ label: 'En savoir plus', link: '/features' }"
    image="/images/hero-image.png"
  />
  <div class="container">
    <h1>Titre Test</h1>
    <UButton color="primary">Mon bouton</UButton>
    <section>
      <h2>Projets récents</h2>
      <ul>
        <li v-for="project in projects" :key="project.id">
          {{ project.title }} - {{ project.description }}
        </li>
      </ul>
    </section>
  </div>
</template>

<script setup lang="ts">
import NPageHero from "@/components/NPageHero.vue";

const projects = [
  {
    id: 1,
    title: "Projet Flutter",
    description: "Application mobile avec Flutter",
  },
  {
    id: 2,
    title: "Rencontre Jeunes-Entreprises",
    description: "Événement avec IBM Lille",
  },
];
</script>

<style scoped>
.container {
  max-width: 800px;
  padding: 2rem;
}
</style>
