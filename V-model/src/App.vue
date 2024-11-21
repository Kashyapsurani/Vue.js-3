<script setup>
import { ref } from 'vue'

// Create reactive references
const name = ref('');
const email = ref('');

const submitForm = () => {
  alert(`Name: ${name.value}\nEmail: ${email.value}`);
};
</script>

<template>
  <h1>Simple Form Example</h1>
  <label for="name">Name:</label>
  <input type="text" id="name" v-model="name" placeholder="Enter your name">

  <label for="email">Email:</label>
  <input type="email" id="email" v-model="email" placeholder="Enter your email">

  <p>Your name is: {{ name }}</p>
  <p>Your email is: {{ email }}</p>

  <button @click="submitForm">Submit</button>

</template>