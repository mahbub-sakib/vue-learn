<script setup>
import { ref } from 'vue';

const name = 'sakib';
function sayName(num) {
  return num + 'sakib'
}

const names = ref(['Sakib', 'Abony', 'Sadiq'])

const inputValue = ref('placeholder value');

function handleInputChange(event){
    inputValue.value = event.target.value;
}

function handleSubmit(event){
    console.log(event);
}

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

  <h1>{{ inputValue }}</h1>

  <input 
  type="text"
  
  v-model = "inputValue"
  >

  <form @submit.prevent="handleSubmit">
    <input type="text" value="value 1">
    <input type="submit" name="" id="">
  </form>

</template>

<style>
.red {
  color: red;
}
</style>
