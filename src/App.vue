<script setup>
  import { ref } from 'vue'
  const name = ref('')
  const project = ref('')
  const text = ref('')
  const reponse = ref(true)

  function toggle() {
    reponse.value = !reponse.value
  }
</script>

<template>
  <h1>Formulaire </h1>
    <input v-model="name" placeholder="Type your name">
    <input v-model="project" placeholder="Type the name of your project">
    <input v-model="text" placeholder="Type text">
  <button @click="toggle">Envoie formulaire</button>
  <p v-if="reponse"></p>
  <p v-else>{{ name }}, {{ project }}, {{ text }}</p>
</template>

<style scoped>
input{
  display: block;
  margin-bottom: 5px;
}
</style>
