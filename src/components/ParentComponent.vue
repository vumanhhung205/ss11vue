<template>
    <div>
      <div v-if="isShow">
          <ChildrenComponent></ChildrenComponent>
      </div>
      <h1>Parent Component</h1>
      <button @click="handleShow">Toggle</button>
    </div>
  </template>
  
  <script setup>
  import ChildrenComponent from './ChildrenComponent.vue';
  import { ref } from 'vue';
  
  const isShow = ref(false);
  const handleShow = () => {
      isShow.value =!isShow.value;
  };
  </script>
  
  <style>
  
  </style>