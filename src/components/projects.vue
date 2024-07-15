<template>
  <v-col class="d-flex mt-5 margin-col" cols="12" offset-md="2">
    <h1>Here You can Discover and Explore My Development Projects!</h1>
  </v-col>
  <v-row class="d-flex justify-center">
    <v-col cols="11" md="4" class="cards-top">
      <card-template :projects="projectsCol1"/>
    </v-col>
    <v-col cols="11" md="4" class="cards-bottom">
      <card-template :projects="projectsCol2"/>
    </v-col>
  </v-row>
</template>

<script setup lang="ts">
import CardTemplate from "@/components/card-template.vue";

const projectsCol1 = [
  {
    title: 'Library',
    description: 'An online library with authentication for borrowing books, creating reading lists, and exploring new books.',
    push: 'https://github.com/otaaaviio/library-repo',
    stacks: ['NESTJS', 'TS', 'POSTGRESQL', 'VUE', 'PRISMA']
  },
  {
    title: 'Redis Implementation',
    description: 'Redis implementation inspired by the CodeCrafters Challenge, showcasing advanced caching and data management skills.',
    push: 'https://github.com/otaaaviio/redis-typescript',
    stacks: ['NODEJS', 'TS']
  },
  {
    title: 'Discord Clone',
    description: 'A full-stack Discord Clone with live messaging, authentication, and robust testing with Mockery and Pest.',
    push: 'https://github.com/otaaaviio/disc-laravel',
    stacks: ['LARAVEL', 'POSTGRESQL', 'SANCTUM', 'PEST', 'MOCKERY']
  },
  {
    title: 'Stock Control',
    description: 'Stock control project developed with the Filament Framework, focusing on efficiency and ease of use.',
    push: 'https://github.com/otaaaviio/controle-de-estoque',
    stacks: ['LARAVEL', 'POSTGRESQL', 'FILAMENT', 'PEST']
  },
]
const projectsCol2 = [
  {
    title: 'Control Academy API',
    description: 'A Spring Boot API for academic management, featuring robust testing and innovative features for modern education.',
    push: 'https://github.com/otaaaviio/control-academy',
    stacks: ['SPRING BOOT', 'POSTGRESQL', 'MOCKITO']
  },
  {
    title: 'Store Management System',
    description: 'Store management system implemented with the Filament Framework, optimizing operations and enhancing user experience.',
    push: 'https://github.com/otaaaviio/filament-store',
    stacks: ['LARAVEL', 'POSTGRESQL', 'FILAMENT']
  },
  {
    title: 'Link Shortener',
    description: 'Link Shortener API using Redis and Laravel for high performance and scalability.',
    push: 'https://github.com/otaaaviio/link-shortener',
    stacks: ['LARAVEL', 'REDIS', 'POSTGRESQL', 'PEST']
  },
]
</script>

<style scoped>
@media (max-width: 960px) {
  .cards-bottom {
    padding-top: 0;
  }
  .cards-top {
    padding-bottom: 0;
  }
}
</style>

