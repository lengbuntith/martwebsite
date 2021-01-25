<template>
  <v-app>
    <nav-bar />
    <catalog-list />

    <router-view />
  </v-app>
</template>

<script>
import CatalogList from './components/CatalogList.vue';
import NavBar from "./components/NavBar"

export default {
  components: { NavBar, CatalogList },
};
</script>

<style scoped>
@import url('https://fonts.googleapis.com/css2?family=Montserrat&display=swap');

* {
  font-family: 'Montserrat', sans-serif;
}
  

</style>