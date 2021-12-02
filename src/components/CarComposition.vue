<template>
  <h2>Auto - Composition API</h2>
  <p>
    Color:
    <!-- <span v-for="(color,index) in colors" :key="index">
       {{index}}: {{color}} -
    </span> -->
  </p>
  <ul>
    <li v-for="(color, index) in colors" :key="index">
      {{ index }}: {{ color }}
    </li>
  </ul>
  <p>Precio: ${{ price }}</p>
  <p>Potencia: {{ power }}</p>
  <button @click="upPower">Aumentar</button>
  <button @click="downPower">Disminuir</button>
</template>

<script>
export default {
  setup() {
    const colors = ["Azul", "Naranja", "Verde", "Rojo", "Cafe", "Amarillo"];
    const price = 45000;
    const power = 40;

    const upPower = () => {
      console.log("Autmentar");
    };
    const downPower = () => {
      console.log("Autmentar");
    };
    return {
      colors,
      price,
      power,
      upPower,
      downPower,
    };
  },
};
</script>

<style></style>
