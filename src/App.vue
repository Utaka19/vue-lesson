<script setup>
import { ref, reactive } from 'vue'
const title = ref('Vue.jd Course')
let price = ref(9.99)
console.log(price.value)
function increment() {
  price.value++
  instructor.age++
}
const info = ref({
    students: 1000,
    rating: 4.0
})
const instructor = reactive({
    name: 'Sei',
    age: 25
})
console.log(instructor.age)
</script>
<template>
  <h1>Title: {{ title }}</h1>
  <h2>Price: ${{ price - 1 }}</h2>
  <button @click="increment">button</button>
  <h2>Students: {{ info.students }}</h2>
  <h2>Instructor age: {{ instructor.age }}</h2>
</template>
