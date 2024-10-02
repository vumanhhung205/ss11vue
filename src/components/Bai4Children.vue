<template>
  <div>
    <p>Received Age: {{ age }}</p>
  </div>
</template>

<script setup>
import { defineProps, watch } from 'vue';

const props = defineProps(['age']);

watch(() => props.age, (newAge, oldAge) => {
  alert(`Giá trị của biến age đã thay đổi: từ ${oldAge} thành ${newAge}`);
});
</script>

<style scoped>
</style>
