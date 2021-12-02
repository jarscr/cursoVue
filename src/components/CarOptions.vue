<template>
  <h2>Auto - Options API</h2>
  <p>Marca: {{ brand }}</p>
  <p>Modelo: {{ model }}</p>
  <p>Potencia: {{ power }}</p>
  <button @click="upPower(1000)">Aumentar</button>
  <button @click="downPower">Disminuir</button>
</template>

<script>
export default {
  data() {
    return {
      brand: "Audi",
      model: "A4",
      power: 50,
    };
  },
  methods:{
      upPower(newPower){
          console.log("Aumentando " + newPower);
      },
      downPower(){
 console.log("Disminuir");
      }
  }
};
</script>

<style></style>
