<script setup>
import { RouterLink, RouterView } from 'vue-router'
</script>

<!-- besoin d'un v-if et d'un ref -->

<template>
    <nav class="bg-gray-800 p-4">
        <div class="container mx-auto flex items-center justify-between">
            <router-link to="/" class="text-white text-lg font-bold">Mon Site</router-link>

            <ul v-if="isOpen" class="flex space-x-4">
                <router-link to="/" class="text-white">Accueil</router-link>
                <router-link to="/about" class="text-white">À Propos</router-link>
                <router-link to="/services" class="text-white">Services</router-link>
                <router-link to="/contact" class="text-white">Contact</router-link>
            </ul>

            <ul v-else class="flex flex-col space-x-4">
                <router-link to="/" class="text-white">Accueil</router-link>
                <router-link to="/about" class="text-white">À Propos</router-link>
                <router-link to="/services" class="text-white">Services</router-link>
                <router-link to="/contact" class="text-white">Contact</router-link>
            </ul>
        </div>
    </nav>
</template>