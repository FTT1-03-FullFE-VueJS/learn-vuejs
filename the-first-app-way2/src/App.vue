<!-- HTML -->
<template>
  <div class="app-container">
    <h1>{{ title }}</h1>
    <button @click="minus">-</button>
    <input type="text" :value="number">
    <button @click="plus">+</button>
    <br>
    <button @click="changeTitle('Today i very happy!')">Change title</button>
  </div>
</template>

<!-- JAVASCIPT -->
<script>
import { ref } from 'vue';

export default {
  data() {
    return {
      title: 'Title 2',
    };
  },
  setup() {
    let title = ref('Counter number application');
    const number = ref(1);

    function changeTitle(titleChanged) {
      title.value = titleChanged;
    }

    function plus() {
      number.value++;
    }

    function minus() {
      number.value--;
    }

    return {
      title,
      number,
      plus,
      minus,
      changeTitle
    };
  },
}
</script>

<!-- CSS -->
<style>
.app-container {
  color: #f00;
}
</style>
