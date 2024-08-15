<template>
  <div class="text-center">
    <!-- <h1 class="">Hijo</h1> -->
  </div>
  <div class="d-flex justify-content-center">
    <div class="text-center mx-auto my-auto">
      <br />
      <button class="ropa btn btn-primary">
        {{ cosa.ropa }} ({{ cosa.marca }})
      </button>
    </div>
    <br />
    <div class="estrellas mx-auto my-auto">
      <span v-for="index in cosa.nota" :key="index">
        <img
          class="estrella"
          src="https://www.html6.es/img/estrella.png"
          alt="estrellas"
        />
      </span>
    </div>
    <br />
    <div class="mx-auto my-auto">
      <button
        @click="incrementarNota(cosa.nota, index)"
        class="btn btn-success"
      >
        +
      </button>
    </div>
  </div>
</template>

<script setup>
const props = defineProps({
  cosa: String,
  index: Number,
});

const emito = defineEmits(["retorno"]);
const incrementarNota = (a, i) => {
  emito("retorno", a, i);
};
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
