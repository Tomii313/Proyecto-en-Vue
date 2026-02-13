
<template>
  
  <h1>Hola bro</h1>
  <p>{{ contador }}</p>
  <button @click="incrementar">Incrementar</button>
  <button @click="decrementar">Decrementar</button>
</template>

<script setup>
import {ref} from 'vue';
const contador = ref(0);

const incrementar = () => {
  contador.value++;
}

const decrementar = () => {
  contador.value -= 1;
}
</script>


<style scoped>
p{
  color:red;
}

</style>
