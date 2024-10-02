<template>
    <div>
        <h1>Bài9</h1>
      <h1>Counter: {{ count }}</h1>
    </div>
  </template>
  
  <script>
  export default {
    data() {
      return {
        count: 0,
        intervalId: null,
      };
    },
    mounted() {
      this.intervalId = setInterval(() => {
        this.count++;
      }, 1000);
    },
    beforeDestroy() {
      clearInterval(this.intervalId);
    },
  };
  </script>
  
  <style scoped>

  </style>
  