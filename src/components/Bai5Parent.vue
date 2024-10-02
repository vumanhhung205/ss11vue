<template>
    <div>
      <h1>Bai5</h1>
      <button @click="toggleChild" class="toggle-btn">Toggle</button>
      <Exercise05Children v-if="isChildVisible" />
    </div>
  </template>
  
  <script setup>
  import { ref } from 'vue';
  import Exercise05Children from './Bai5Children.vue'; 
    const isChildVisible = ref(false);
  
  const toggleChild = () => {
    isChildVisible.value = !isChildVisible.value;
  };
  </script>
  
  <style scoped>
  </style>
  