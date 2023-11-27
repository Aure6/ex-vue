<script setup>
import { RouterLink, RouterView } from 'vue-router'
// import HelloWorld from './components/HelloWorld.vue'
import ButtonComponent from '/src/components/ButtonComponent.vue'
import TitleComponent from '/src/components/TitleComponent.vue'
import NavbarComponent from '/src/components/NavbarComponent.vue'
import ContactFormComponent from '/src/components/ContactFormComponent.vue'

</script>

<template>
    <div class="p-4">
        <h2 class="text-5xl">Les boutons</h2>
        <div>
            <ButtonComponent type="primary">Bouton Principal</ButtonComponent>
            <ButtonComponent type="success">Bouton Succès</ButtonComponent>
            <ButtonComponent type="danger">Bouton Danger</ButtonComponent>
            <ButtonComponent type="secondary">Bouton Secondaire</ButtonComponent>
            <ButtonComponent>Bouton par défaut</ButtonComponent>
        </div>
        <div>
            <h2 class="text-5xl">Les titres</h2>
            <TitleComponent level="h1">Titre H1</TitleComponent>
            <TitleComponent level="h2">Titre H2</TitleComponent>
            <TitleComponent level="h3">Titre H3</TitleComponent>
            <TitleComponent level="h4">Titre H1</TitleComponent>
            <TitleComponent level="h5">Titre H2</TitleComponent>
            <TitleComponent level="h6">Titre H3</TitleComponent>
            <!-- Ajoutez d'autres instances avec différents niveaux au besoin -->

        </div>

    </div>
</template>