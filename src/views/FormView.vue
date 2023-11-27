<script setup>
import { RouterLink, RouterView } from 'vue-router'
import NavbarComponent from '/src/components/NavbarComponent.vue'
import ContactFormComponent from '/src/components/ContactFormComponent.vue'

</script>

<template>
    <main class="p-4">
        <h2 class="text-5xl">Formulaire</h2>
        <ContactFormComponent>

        </ContactFormComponent>

    </main>
    <!-- <RouterView /> -->
</template>