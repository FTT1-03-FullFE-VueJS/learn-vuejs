<template>
  <!-- <div data-number="1" v-if="number === 1">This is Number 1</div>
  <div data-number="2" v-else-if="number === 2">This is Number 2</div>
  <div data-number="3" v-else-if="number === 3">This is Number 3</div>
  <div data-number="another" v-else>This is Another Number</div> -->
  <!-- <div data-number="1" v-show="number === 1">This is Number 1</div>
  <div data-number="2" v-show="number === 2">This is Number 2</div>
  <div data-number="3" v-show="number === 3">This is Number 3</div>
  <div data-number="another" v-show="![1 , 2, 3].includes(number)">This is Another Number</div> -->
  <div>
    <ul>
      <li v-for="(item, index) in products" :key="index">
        <div>ID: {{ item.id }}</div>
        <div>-</div>
        <div>Name: {{ item.name }}</div>
        <div>-</div>
        <div>Price: ${{ item.price }}</div>
        <div>------------------------------</div>
      </li>
    </ul>
  </div>
</template>

<script setup>
import { ref } from 'vue';

const number = ref(1);
const products = ref([
  {
    id: 1,
    name: 'Quan A',
    price: 100
  },
  {
    id: 2,
    name: 'Quan B',
    price: 200
  },
  {
    id: 3,
    name: 'Quan C',
    price: 300
  },
  {
    id: 4,
    name: 'Quan D',
    price: 400
  },
]);

products.value = products.value.filter(item => item.price > 100);

function randomIntFromInterval(min, max) { // min and max included
  return Math.floor(Math.random() * (max - min + 1) + min)
}

number.value = randomIntFromInterval(1, 6);

/**
 * Lưu ý:
 * - Không được dùng chung v-if với v-for
 */
</script>

<style>

</style>