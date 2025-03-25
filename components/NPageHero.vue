<template>
  <section
    class="bg-secondary-50 dark:bg-secondary-900 py-16 px-8 rounded-2xl shadow-lg"
  >
    <div
      class="container mx-auto grid grid-cols-1 md:grid-cols-2 gap-10 items-center"
      style="display: flex; justify-content: space-between; padding: 10em 0"
    >
      <!-- Contenu principal -->
      <div>
        <h1
          class="text-4xl font-bold text-primary-900 dark:text-primary-100 leading-snug"
        >
          {{ title }}
        </h1>
        <p class="mt-4 text-lg text-primary-700 dark:text-primary-300">
          {{ description }}
        </p>
      </div>
      <div class="mt-6 flex gap-4">
        <NuxtLink
          v-if="primaryAction"
          :to="primaryAction.link"
          class="bg-primary-500 secondary-text px-6 py-3 rounded-lg shadow-md hover:bg-primary-600 transition"
        >
          {{ primaryAction.label }}
        </NuxtLink>

        <NuxtLink
          v-if="secondaryAction"
          :to="secondaryAction.link"
          class="bg-white border border-primary-500 text-primary-500 px-6 py-3 rounded-lg shadow-md hover:bg-primary-50 transition"
        >
          {{ secondaryAction.label }}
        </NuxtLink>
      </div>

      <!-- Image -->
      <!-- <div v-if="image" class="flex justify-center">
        <img
          :src="image"
          :alt="title"
          class="rounded-lg shadow-md w-full max-w-sm"
        />
      </div> -->
    </div>
  </section>
</template>

<script setup lang="ts">
defineProps({
  title: {
    type: String,
    required: true,
  },
  description: {
    type: String,
    required: true,
  },
  primaryAction: {
    type: Object,
    default: null,
  },
  secondaryAction: {
    type: Object,
    default: null,
  },
  image: {
    type: String,
    default: null,
  },
});
</script>

<style scoped>
/* Ajoutez ici vos styles personnalisés si nécessaire */
</style>
