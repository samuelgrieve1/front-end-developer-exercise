<template>
  <b-container>
    <b-row class="my-5">
      <b-col>
        <h1 class="website-title">Company Inc.</h1>
        <NuxtLink to="/">Home</NuxtLink>
        <NuxtLink to="pricing">Pricing</NuxtLink>
      </b-col>
      <b-col>
        <dark-mode />
      </b-col>
    </b-row>
    <b-row>
      <Nuxt />
    </b-row>
  </b-container>
</template>

<script>
import '../assets/custom.css';
import '../assets/dark.css';
import DarkMode from "@/components/DarkMode.vue";

export default {
  name: 'Default',
  components: { DarkMode }
};
</script>