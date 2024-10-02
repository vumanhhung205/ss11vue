<template>
  <div>
    <h1>Bài 2</h1>
    <p>Giá trị count: {{ count }}</p>
    <button @click="incrementCount">Counter</button>
  </div>
</template>

<script setup>
import { ref, watch } from 'vue';
const count = ref(0);

const incrementCount = () => {
  count.value++;
};

watch(count, (newVal, oldVal) => {
  console.log(`Dữ liệu đã thay đổi: count thay đổi từ ${oldVal} thành ${newVal}`);
});
</script>

<style >
</style>
