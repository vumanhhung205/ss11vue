<template>
    <div>
        <h1>Bài8</h1>
      <h1>Chiều rộng cửa sổ: {{ windowWidth }}px</h1>
      <p>Màn hình khi resize còn {{ windowWidth }}px</p>
    </div>
  </template>
  
  <script setup>
  import { ref, onMounted, onUnmounted } from 'vue';
  
  const windowWidth = ref(window.innerWidth);
  
  const updateWindowWidth = () => {
    windowWidth.value = window.innerWidth;
  };
  
  onMounted(() => {
    window.addEventListener('resize', updateWindowWidth);
  });
  
  onUnmounted(() => {
    window.removeEventListener('resize', updateWindowWidth);
  });
  </script>
  
  <style scoped>
  </style>
  