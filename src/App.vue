<script setup>
import { RouterLink, RouterView } from 'vue-router'
// import HelloWorld from './components/HelloWorld.vue'
import ButtonComponent from '/src/components/ButtonComponent.vue'
import TitleComponent from '/src/components/TitleComponent.vue'
import NavbarComponent from '/src/components/NavbarComponent.vue'
import ContactFormComponent from '/src/components/ContactFormComponent.vue'

</script>

<template>
  <header>
    <!-- <img alt="Vue logo" class="logo" src="@/assets/logo.svg" width="125" height="125" /> -->
    <NavbarComponent />
  </header>
  <RouterView />
</template>