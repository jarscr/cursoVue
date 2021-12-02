<template>
  <h1>Nuestro primer componente VueJS</h1>
  <CarOptions />
  <CarComposition />
</template>

<script>
import CarComposition from "./components/CarComposition";
import CarOptions from "./components/CarOptions";

export default {
  components: {
    CarComposition,
    CarOptions,
  },
};
</script>

<style></style>
