<script setup>
import { RouterLink, RouterView } from 'vue-router'
import FooterComponent from './components/FooterComponent.vue'
import mystyles from './assets/mystyles.css'

</script>

<template>
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<meta charset="UTF-8">

  <div class="nav-container">
    <!-- <input type="checkbox" id="menu-toggle" class="menu-toggle" />
    <label for="menu-toggle" class="dropdown-btn">Menu</label> -->
    <div class="links-container">
      <RouterLink class="nav-link" to="/">Home</RouterLink>
      <RouterLink class="nav-link" to="/about">About</RouterLink>
      <RouterLink class="nav-link" to="/contact">Contact</RouterLink>

    </div>
  </div>

  <div class="page-container">
    <div class="content-wrapper">
  <RouterView />
  </div>

  <footer class="amazing-footer">

    <FooterComponent />
  </footer>
  </div>
</template>


<style scoped>


</style>