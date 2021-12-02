<template>
  <h2>Auto - Composition API</h2>
  <p>Marca: {{ brand }}</p>
  <p>Modelo: {{ model }}</p>
  <p>Potencia: {{ power }}</p>
  <button @click="upPower">Aumentar</button>
  <button @click="downPowerFn">Disminur</button>
</template>

<script>
export default {
    props: {
        power: {
            type: String,
            default: 60
        },
        upPower : Function,
    },
    emits : ["downPower"],
  setup(props,context) {


    const brand =  "Audi";
    const model = "A4";   

    const downPowerFn = () => {
        context.emit("downPower");
    }
  
    return {
     
      model,
      brand,
      downPowerFn,
     
    };
  },
};
</script>

<style></style>
