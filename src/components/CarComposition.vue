<template>
  <h2>Auto - Composition API</h2>
  <p>Marca: {{ brand }}</p>
  <p>
    Color:
  <span v-for="(color,index) in colors" :key="index">
       {{index}}: {{color}} -
    </span>
  </p>
  <ul>
    <li v-for="(color, index) in colors" :key="index">
      {{ index }}: {{ color }}
    </li>
  </ul>
  <p>Precio: ${{ price }}</p>
  <p>Potencia: {{ power }}</p>
  <button @click="upPower(20)">Aumentar</button>
  <button @click="downPower(20)">Disminuir</button>
</template>

<script>
import { ref } from "vue";
export default {
  setup() {
    const colors = ["Azul", "Naranja", "Verde", "Rojo", "Cafe", "Amarillo"];
    const price = 45000;
    const brand =  "Audi";
    const model = "A4";
    let power = ref(40);

    const upPower = (newPower) => {
      // console.log("Autmentar");
      power.value = power.value + newPower;
      //console.log(power.value);
    };
    const downPower = (newPower) => {
      power.value = power.value - newPower;
    };
    return {
      colors,
      price,
      power,
      model,
      brand,
      upPower,
      downPower,
    };
  },
};
</script>

<style></style>
