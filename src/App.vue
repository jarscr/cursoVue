<template>
  <h1>VueJS</h1>
  <Car :power="power" :upPower="upPower" @downPower="downPower"/>
</template>

<script>
import {ref} from "vue";
import Car from "./components/Car";

export default {
  components: {
    Car,
  },
  setup (){
    let power = ref(30);

    const upPower = () => {
      power.value++;
    }

     const downPower = () => {
      power.value--;
    }

    return {
      power,
      upPower,
      downPower,
    }
  }
};
</script>

<style></style>
