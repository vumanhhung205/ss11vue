<template>
    <div>
        <h1>Bài7</h1>
      <h1>{{ title }}</h1>
      <input v-model="inputValue" placeholder="Nhập tên công ty" />
    </div>
  </template>
  
  <script setup>
  import { ref, watch } from 'vue';
  
  const title = ref('Rikkei Education');
  
 const inputValue = ref('');
  
  watch(inputValue, (newVal) => {
    document.title = newVal || title.value; 
  });
  </script>
  
  <style scoped>  </style>
  