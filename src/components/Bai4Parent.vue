<template>
  <div>
    <h1>Bai4</h1>
    <p>Current Age: {{ age }}</p>
    <button @click="increaseAge" class="increase-btn">Increase age</button>
    <Exercise03Children :age="age" />
  </div>
</template>

<script setup>
import { ref } from 'vue';
import Exercise03Children from './Bai4Children.vue';

const age = ref(1);
const increaseAge = () => {
  age.value++;
};
</script>

<style scoped>

</style>
