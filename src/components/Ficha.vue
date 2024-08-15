<template>
  <div class="text-center">
    <!-- <h1>Hijo</h1> -->
  </div>
  <div class="d-flex justify-content-center">
    <div class="text-center">
      <br />
      <button class="ropa btn btn-primary">
        {{ cosa.ropa }} ({{ cosa.marca }})
      </button>
    </div>
    <br />
    <div class="estrellas">
      <span v-for="index in cosa.nota" :key="index">
        <img
          class="estrella"
          src="https://www.html6.es/img/estrella.png"
          alt="estrellas"
        />
      </span>
    </div>
    <br />
    <div class="">
      <button class="btn btn-success">+</button>
    </div>
  </div>
</template>

<script setup>
const props = defineProps({
  cosa: String,
  index: Number,
});
</script>

<style lang="css" scoped>
.estrella {
  width: 15px;
  margin: 5px;
}
button {
  width: 100px;
  margin: 10px;
}
.ropa {
  width: 250px;
}
.estrellas {
  width: 150px;
}
</style>
