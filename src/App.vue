<template>
  <br><br>
  <div class="text-center">
    <!-- <h1>Padre</h1> -->
  </div>
  <div v-for="(cosa,index) in cosas" :key="index" class="text-center">
    <FichaVue :cosa="cosa" :index="index" />
  </div>

</template>

<script setup>
  import FichaVue from './components/Ficha.vue';
  import cosas from './assets/datos.js';

</script>

<style lang="css" scoped>

</style>