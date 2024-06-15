<template>
  <v-app id="inspire" class="body">
    <v-app-bar flat elevation="10" rounded color="transparent">
      <v-container class="mx-auto d-flex align-center justify-center max-width bg">
        <v-btn
          v-for="link in links"
          :key="link"
          :text="link.title"
          :class="link.step === step ? 'elevation-2' : 'elevation-0'"
          class="mr-2 ml-2"
          @click="handleStep(link.step)"
          variant="text"
        />
        <v-spacer></v-spacer>
        <a
          v-for="item in items"
          :key="item.title"
          :href="item.href"
          :title="item.title"
          class="d-inline-block mx-3 social-link no-color"
          rel="noopener noreferrer"
          target="_blank"
        >
          <v-icon
            :icon="item.icon"
            :size="24"
          />
        </a>
      </v-container>
    </v-app-bar>
    <v-main class="mt-5">
      <v-window v-model="step">
        <v-window-item :value="1">
          <projects/>
        </v-window-item>
        <v-window-item :value="2">
          <about/>
        </v-window-item>
        <v-window-item :value="3">
        </v-window-item>
      </v-window>
      <app-footer/>
    </v-main>
  </v-app>
</template>

<script setup>
import Projects from "@/components/projects.vue";
import About from "@/components/about.vue";
import AppFooter from "@/components/app-footer.vue";

const links = [
  {title: 'Projects', step: 1},
  {title: 'About me', step: 2},
  // {title: 'Articles', step: 3},
]

const items = [
  {
    title: 'Linkedin',
    icon: 'mdi-linkedin',
    href: 'https://www.linkedin.com/in/otaaaviio/',
  },
  {
    title: 'Twitter',
    icon: `svg:M2.04875 3.00002L9.77052 13.3248L1.99998 21.7192H3.74882L10.5519 14.3697L16.0486 21.7192H22L13.8437 10.8137L21.0765 3.00002H19.3277L13.0624 9.76874L8.0001 3.00002H2.04875ZM4.62054 4.28821H7.35461L19.4278 20.4308H16.6937L4.62054 4.28821Z`,
    href: 'https://x.com/OtaTargaryen_',
  },
  {
    title: 'GitHub',
    icon: `mdi-github`,
    href: 'https://github.com/otaaaviio',
  },
]
</script>

<script>
export default {
  data: () => ({
    step: 1,
  }),
  methods: {
    handleStep(value) {
      this.step = value
    },
  },
}
</script>

<style>
.max-width {
  max-width: 1400px;
}

.no-color {
  color: inherit;
}

.body {
  background: url('https://www.toptal.com/designers/subtlepatterns/uploads/ep_naturalblack.png') !important;
}
</style>
