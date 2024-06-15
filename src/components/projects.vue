<template>
  <v-row class="d-flex justify-space-evenly mt-5">
    <h1>Here You can Discover and Explore My Development Projects</h1>
    <div/>
  </v-row>
  <v-row class="d-flex justify-center">
    <v-col cols="4">
      <card-template :projects="projectsCol1"/>
    </v-col>
    <v-col cols="4">
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
    stacks: ['LARAVEL', 'PHP', 'POSTGRESQL', 'SANCTUM', 'PEST', 'MOCKERY']
  },
  {
    title: 'Stock Control',
    description: 'A stock control project. Check out the GitHub repository for more information.',
    push: 'https://github.com/otaaaviio/controle-de-estoque',
    stacks: ['LARAVEL', 'PHP', 'POSTGRESQL', 'FILAMENT', 'PEST']
  },
]
const projectsCol2 = [
  {
    title: 'Control Academy API',
    description: 'A Spring Boot project for managing an academic environment with robust tests. More details can be found on its GitHub page.',
    push: 'https://github.com/otaaaviio/control-academy',
    stacks: ['SPRING BOOT', 'JAVA', 'POSTGRESQL', 'MOCKITO']
  },
  {
    title: 'Store Management System',
    description: 'A store management system project implemented with Filament. For a comprehensive overview, visit the GitHub.',
    push: 'https://github.com/otaaaviio/udep-store',
    stacks: ['LARAVEL', 'PHP', 'POSTGRESQL', 'FILAMENT']
  },
]
</script>

