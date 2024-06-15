<template>
  <v-footer height="40" app class="bg-transparent elevation-10">
    <div
      class="text-caption text-disabled no-color bg"
      style="position: absolute; right: 16px;">
      &copy; {{ (new Date()).getFullYear() }} <span class="d-none d-sm-inline-block">Otávio G.</span>
      —
      <a
        class="text-decoration-none on-surface"
        href="https://vuetifyjs.com/about/licensing/"
        rel="noopener noreferrer"
        target="_blank"
      >
        My Portfolio
      </a>
    </div>
  </v-footer>
</template>

<style>
.no-color {
  color: inherit;
}
</style>
