<template>
  <h1>Hola mundo</h1>
  <p>{{ contador }}</p>
  <button @click="incrementar">Incrementar</button>
  <button @click="decrementar">Decrementar</button>
 </template>

<script setup>
import { ref } from 'vue';
const contador = ref(1);
const incrementar = () => {
  contador.value++;
  if (contador.value === 10) {
    contador.value = 0;
}
}

const decrementar = () => {
  contador.value--;
}

</script>

<style scoped>
p{
  color: blueviolet;
  text-align: center;
}
h1{
  color: aquamarine;
  text-align: center;
}
button{
  color: black;
  text-align: center;
  align-items: center;
  display: flex;
  justify-content: center;
}
</style>
