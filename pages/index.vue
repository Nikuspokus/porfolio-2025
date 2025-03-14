<template>
  <div class="container">
    <h1>Titre Teset</h1>
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

<script setup>
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
