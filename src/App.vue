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

    <!-- <div class="wrapper">
                      <HelloWorld msg="You did it!" />
                      <nav>
                        <RouterLink to="/">Home</RouterLink>
                        <RouterLink to="/about">About</RouterLink>
                      </nav>
                    </div> -->
  </header>
  <div class="p-4">
    <h2>Les boutons</h2>
  <div>
    <ButtonComponent type="primary">Bouton Principal</ButtonComponent>
      <ButtonComponent type="success">Bouton Succès</ButtonComponent>
      <ButtonComponent type="danger">Bouton Danger</ButtonComponent>
      <ButtonComponent type="secondary">Bouton Secondaire</ButtonComponent>
      <ButtonComponent>Bouton par défaut</ButtonComponent>
    </div>
    <div>
      <h2>Les tires</h2>
      <!-- <TitleComponent level="h1">Titre de niveau 1</TitleComponent>
                                            <TitleComponent level="h2">Titre de niveau 2</TitleComponent>
                                            <TitleComponent level="h3">Titre de niveau 3</TitleComponent> -->
      <TitleComponent level="h1">Titre H1</TitleComponent>
      <TitleComponent level="h2">Titre H2</TitleComponent>
      <TitleComponent level="h3">Titre H3</TitleComponent>
      <TitleComponent level="h4">Titre H1</TitleComponent>
      <TitleComponent level="h5">Titre H2</TitleComponent>
      <TitleComponent level="h6">Titre H3</TitleComponent>
      <!-- Ajoutez d'autres instances avec différents niveaux au besoin -->

    </div>
    <ContactFormComponent>

    </ContactFormComponent>
  </div>
  <!-- <RouterView /> -->
</template>