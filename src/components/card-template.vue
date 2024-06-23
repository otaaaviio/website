<template>
  <v-card
    v-for="(item, index) in projects" :key="index"
    variant="tonal"
    elevation="10"
    class="mb-5 d-flex flex-column outlined-card"
    height="250"
    :href="item.push"
    target="_blank"
  >
    <v-card-title>{{ item.title }}</v-card-title>
    <v-card-text>{{ item.description }}</v-card-text>
    <v-spacer/>
    <v-divider class="mx-3"/>
    <v-card-title>Stacks:</v-card-title>
    <v-card-actions>
      <v-btn v-for="(stack, key) in item.stacks" :key="key" class="rounded" elevation="2" color="blue">
        {{ stack }}
      </v-btn>
    </v-card-actions>
  </v-card>
</template>

<script lang="ts">
import { Project } from '@/interfaces/project'

export default {
  props: {
    projects: {
      type: Array as () => Project[],
      required: true,
    },
  },
}
</script>

<style scoped>
.outlined-card {
  border: 1px solid cornflowerblue;
}
</style>
