<script setup>
import { ref } from 'vue'

const count = ref(0); 
const inputValue = ref(''); 

const increment = () => {
  count.value++; 
};

const decrement = () => {
  count.value--; 
};

const reset = () => {
  count.value = 0; 
};

const setCount = () => {
  count.value = parseInt(inputValue.value) || 0;
};
</script>

<template>
  <h1>Counter: {{ count }}</h1>
  <button @click="increment">Increment</button>
  <button @click="decrement">Decrement</button>
  <button @click="reset">Reset</button>
  <input type="text" placeholder="Enter a value" v-model="inputValue">
  <button @click="setCount">Set Count</button>

</template>