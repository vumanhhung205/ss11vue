<template>
    <div>
        <h1>Bai6</h1>
      <h1>Count: {{ count }}</h1>
      <button @click="incrementCount" class="increment-btn">Increment</button>
    </div>
  </template>
  
  <script setup>
  import { ref, watch } from 'vue';
  
  const count = ref(0);
    const incrementCount = () => {
    count.value++;
  };
  
  watch(count, (newCount) => {
    document.title = `Count: ${newCount}`; 
  });
  </script>
  
  <style scoped>

  </style>
  