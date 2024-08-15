<template>
  <div class="container bg-dark">
    <br /><br />
    <div class="text-center">
      <br />
      <h1 class="text-white">Valora los productos de mi tienda</h1>
    </div>
    <div v-for="(cosa, index) in cosas" :key="index" class="text-center">
      <FichaVue :cosa="cosa" :index="index" @retorno="retorno" />
    </div>
  </div>
</template>

<script setup>
import FichaVue from "./components/Ficha.vue";
import cosas from "./assets/datos.js";

const retorno = (a, i) => {
  if (a >= 6) {
    cosas.value[i].nota = 1;
  } else {
    cosas.value[i].nota = a + 1;
  }
};
</script>

<style lang="css" scoped></style>
