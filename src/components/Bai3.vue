<template>
    <div>
      <h1>Bài 3</h1>
      <p>Age: {{ age }}</p>
      <p>Current Company: {{ selectedCompany }}</p>
      <button @click="randomizeAge" class="random-btn">Random</button>
    </div>
  </template>
  
  <script setup>
  import { ref, watch } from 'vue';
  
  const age = ref(1);
  
  const companies = ["Rikkei Academy", "Rikkei Education", "Rikkei Fukuoka"];
  
  const selectedCompany = ref(companies[0]);
  
  const randomizeAge = () => {
    age.value = Math.floor(Math.random() * 10) + 1;
  };
  
  watch(age, (newAge) => {
    selectedCompany.value = companies[(newAge - 1) % companies.length];
  });
  </script>
  
  <style scoped>
  .random-btn {
    background-color: blue; 
}
  </style>
  