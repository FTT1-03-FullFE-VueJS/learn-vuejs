<template>
  <div id="container">
    <button @click="counter++">{{counter}}</button>
  </div>
</template>

<script setup>
import { onMounted, onUpdated, ref, reactive, onUnmounted, onActivated } from 'vue';

// const counter = ref(1);

// onUpdated(() => {
//   // console.log('on updated ran!');
// });

// onActivated(() => {
//   console.log('called on initial mount');
// });

// onMounted(function() {
//   const containerEl = document.querySelector('#container');
//   console.log(containerEl);
// });

// onMounted(() => {
//   const containerEl = document.querySelector('#container');
//   console.log(containerEl);
// });

// onUnmounted(() => {
//   // console.log('Vue die');
// });
</script>
