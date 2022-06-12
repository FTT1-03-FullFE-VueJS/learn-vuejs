<!-- HTML -->
<template>
  <div>
    <input type="text" v-model.number="numberA">
    <input type="text" v-model.number="numberB">
    <div :style="{
      marginTop: '10px',
    }">
      <button @click="caculator">GET RESULT</button>
    </div>
    <div>
      <p>Result is: {{ result }}</p>
      <p>{{ result }} is a: {{ typeOfResult }}</p>
    </div>
  </div>
</template>

<!-- JS -->
<script setup>
import { ref, computed, watch } from 'vue';
const numberA = ref(1);
const numberB = ref(2);
const result  = ref(null);

function caculator() {
  console.log('Caculator handler');
  result.value = numberA.value + numberB.value;
}

watch(numberA, (newValue, oldValue) => {
  console.log({
    'oldValue': oldValue,
    'newValue': newValue
  });
});

const typeOfResult = computed(() => {
  if (result.value === null) return '';
  if (result.value % 2 === 0) {
    return 'Even';
  }

  return 'Odd';
});
</script>
<!-- CSS -->
<style>
</style>
