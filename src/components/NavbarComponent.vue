<script setup>
import { ref } from 'vue'
import { RouterLink, RouterView } from 'vue-router'

const isOpen = ref(false)
</script>

<!-- besoin d'un v-if et d'un ref -->

<template>
    <nav class="bg-gray-800 p-4">
        <div class="container mx-auto flex items-center justify-between">
            <router-link to="/" class="text-white text-lg font-bold">Mon Site</router-link>

            <!-- Mobile menu button -->
            <button class="text-white md:hidden  " @click="isOpen = !isOpen">
                {{ isOpen ? 'Fermer' : 'Ouvrir' }}
                <svg viewBox="0 0 24 24" class="w-6 h-6 fill-current">
                    <path fill-rule="evenodd"
                        d="M4 5h16a1 1 0 0 1 0 2H4a1 1 0 1 1 0-2zm0 6h16a1 1 0 0 1 0 2H4a1 1 0 0 1 0-2zm0 6h16a1 1 0 0 1 0 2H4a1 1 0 0 1 0-2z">
                    </path>
                </svg>
            </button>

            <ul v-if="isOpen" class="flex flex-col space-x-4 text-white md:hidden">
                <h2>Menu mobile</h2>
                <router-link to="/">Accueil</router-link>
                <router-link to="/about">À Propos</router-link>
                <router-link to="/services">Services</router-link>
                <router-link to="/contact">Contact</router-link>
            </ul>


            <ul v-else class="hidden md:flex space-x-4 text-white  md:visible ">
                <h2>Menu large</h2>
                <router-link to="/">Accueil</router-link>
                <router-link to="/about">À Propos</router-link>
                <router-link to="/services">Services</router-link>
                <router-link to="/contact">Contact</router-link>
            </ul>
        </div>
    </nav>
</template>