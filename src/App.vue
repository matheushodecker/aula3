<script setup>

import { ref, reactive, computed } from 'vue';

const contador1 = ref(0);
const contador2 = ref(0);
const somartudo = ref(0);
function incrementar1(){
  contador1.value++;
}
function incrementar2(){
  contador2.value++;
}
function decrementar1(){
  contador1.value--;
}
function decrementar2(){
  contador2.value--;
}
function resetar1(){
  contador1.value = 0
}
function resetar2(){
  contador2.value = 0
}
function soma(){
 somartudo.value = contador1.value + contador2.value
  
}
</script>

<template>
  <div class="contador1"></div>
    <div>
    <h1>Contador</h1>
    <p> {{ contador1 }} </p>
    <button @click="incrementar1">Incrementar</button>
    <button @click="decrementar1">Decrementar</button>
    <button @click="resetar1">Reiniciar</button>
  </div>
  <div class="contador1"></div>
    <div>
    <h1>Contador</h1>
    <p> {{ contador2 }} </p>
    <button @click="incrementar2">Incrementar</button>
    <button @click="decrementar2">Decrementar</button>
    <button @click="resetar2">Reiniciar</button>
  </div>
  <button @click="soma">Somar</button>
  <p>{{ somartudo }}</p>
</template>

<style scoped>
header {
  line-height: 1.5;
}

.logo {
  display: block;
  margin: 0 auto 2rem;
}

@media (min-width: 1024px) {
  header {
    display: flex;
    place-items: center;
    padding-right: calc(var(--section-gap) / 2);
  }

  .logo {
    margin: 0 2rem 0 0;
  }

  header .wrapper {
    display: flex;
    place-items: flex-start;
    flex-wrap: wrap;
  }
}
</style>
