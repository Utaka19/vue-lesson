<script setup>
import { ref } from 'vue'
const title = ref('Vue.jd Course')
let price = ref(9.99)
console.log(price.value)
function increment() {
  price.value++
  console.log(price.value)
}
const info = ref({
    students: 1000,
    rating: 4.0
})
console.log(info.value.students)
</script>
<template>
  <h1>Title: {{ title }}</h1>
  <h2>Price: ${{ price - 1 }}</h2>
  <button @click="increment">button</button>
  <h2>Students: {{ info.students }}</h2>
</template>
