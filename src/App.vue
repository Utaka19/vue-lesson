<script setup>
import { ref } from 'vue'
const title = 'Vue.jd Course'
let price = ref(9.99)
console.log(price.value)
function increment() {
  price.value++
  console.log(price.value)
}
</script>
<template>
  <h1>Title: {{ title }}</h1>
  <h2>Price: ${{ price - 1 }}</h2>
  <button @click="increment">button</button>
</template>
