<script setup>
import { ref } from 'vue';

const name = 'sakib';
function sayName(num) {
  return num + 'sakib'
}

const names = ref(['Sakib', 'Abony', 'Sadiq'])

</script>

<template>
  <h1 class="red">Hellow world!!!</h1>

  <div>{{ false ? 'hello' : 'bye' }} {{ name }}</div>
  <div>{{ sayName(10) }}</div>

  <h1 v-if="false">My name is {{ sayName(10) }}</h1>
  <h1 v-else-if="false">My name is Abony</h1>
  <h1 v-else>My name is Sadiq</h1>

  <h1 v-for="(number, index) in names">
    {{ number }} {{ index }}
  </h1>

</template>

<style>
.red {
  color: red;
}
</style>
