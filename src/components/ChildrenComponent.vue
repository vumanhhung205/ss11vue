
<template>
<div>
  <h1>children component</h1>
  <input type="text" v-model="inputValue">
  <h2>Count: {{ count }}</h2>
</div>
</template>

<script setup>
import { onBeforeMount, onBeforeUpdate, onMounted, ref } from 'vue';

const count = ref(0);
const inputValue = ref("")

onBeforeMount(() => {
  count.value = 5;
  console.log("Component before mount");
});

onMounted(() => {
    const count = 6;
    console.log("Component mounted");
});

onBeforeUpdate(() => {
    document.title = inputValue.value;
    console.log("Before update");
})


</script>

<style>

</style>