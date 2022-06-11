<!-- HTML -->
<template>
  <div class="app-container">
    <h1>{{ title }}</h1>
    <div>
      <button @click="minus">-</button>
      <input type="number" :value="number">
      <button @click="plus">+</button>
    </div>
  </div>
</template>

<!-- JAVASCRIPT -->
<script>
export default {
  data() {
    return {
      title: 'Counter number application',
      number: 1,
    };
  },
  methods: {
    plus() {
      console.log('Plus number');
      this.number++;
    },
    minus() {
      console.log('Minus number');
      this.number--;
    }
  },
  setup() {

  },
}
</script>

<!-- CSS -->
<style>
.app-container {
  color: #f00;
  width: 100vw;
  overflow: hidden;
  height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  flex-direction: column;
}
button {
  font-size: 20px;
  padding: 10px 20px;
}
input {
  font-size: 16px;
  padding: 10px;
}
</style>
