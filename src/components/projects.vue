<template>
  <v-col class="d-flex mt-5 margin-col" cols="12" offset-md="2">
    <h1>Here You can Discover and Explore My Development Projects</h1>
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
    description: 'An online library with authentication for borrowing books, creating reading lists, and exploring new books. Full project details are available on GitHub.',
    push: 'https://github.com/otaaaviio/library-repo',
    stacks: ['NESTJS', 'TS', 'POSTGRESQL', 'VUE', 'PRISMA']
  },
  {
    title: 'Discord Clone',
    description: 'A full-stack Discord Clone project with live messages, authentication and mockery and pest tests. Visit GitHub for a complete overview.',
    push: 'https://github.com/otaaaviio/disc-laravel',
    stacks: ['LARAVEL', 'POSTGRESQL', 'SANCTUM', 'PEST', 'MOCKERY']
  },
  {
    title: 'Stock Control',
    description: 'A stock control project. Check out the GitHub repository for more information.',
    push: 'https://github.com/otaaaviio/controle-de-estoque',
    stacks: ['LARAVEL', 'POSTGRESQL', 'FILAMENT', 'PEST']
  },
]
const projectsCol2 = [
  {
    title: 'Control Academy API',
    description: 'A Spring Boot project for managing an academic environment with robust tests. More details can be found on its GitHub page.',
    push: 'https://github.com/otaaaviio/control-academy',
    stacks: ['SPRING BOOT', 'POSTGRESQL', 'MOCKITO']
  },
  {
    title: 'Store Management System',
    description: 'A store management system project implemented with Filament. For a comprehensive overview, visit the GitHub.',
    push: 'https://github.com/otaaaviio/filament-store',
    stacks: ['LARAVEL', 'POSTGRESQL', 'FILAMENT']
  },
  {
    title: 'Link Shortener',
    description: 'A Link Shortener API implmented with Redis. For more details, access the GitHub',
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

