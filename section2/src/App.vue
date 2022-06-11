<template>
  <div ref="appContainer" class="app-container">
    <h1>{{ title }}</h1>
    <form action="" @submit.prevent="register">
      <input type="text" placeholder="Enter the username" v-model="form.username">
      <br>
      <input type="text" placeholder="Enter the email" v-model="form.email">
      <br>
      <input type="text" placeholder="Enter the phone" v-model="form.phone">
      <br>
      <input type="password" placeholder="Enter the password" v-model="form.password">
      <br>
      <button type="submit">Register</button>
    </form>
  </div>
</template>

<script setup>
import { ref, reactive } from 'vue';

// const username = ref('username test');
// const email = ref('email test');
// const phone = ref('phone test');
// const password = ref('password test');

const form = reactive({
  username: '',
  email: '',
  phone: '',
  password: ''
});

let title = reactive(1);// let title = 1

function register(e) {
  console.log('Handle submit form');
  console.log(form);
  // console.log(title);
  title = 2;
}
</script>

<style>
</style>
