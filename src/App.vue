<script setup>
import { ref, reactive } from 'vue'
const title = ref('Vue.jd Course')
let price = ref(9.99)
console.log(price.value)
function increment() {
  price.value++
  instructor.age++
  instructor.bio = 'hi'
  instructor.sns.twitter = 'hello'
}
const info = ref({
    students: 1000,
    rating: 4.0
})
const instructor = reactive({
    name: 'Sei',
    age: 25,
    sns: {
        twitter: '@sei',
        youtube: '@sei_channel'
    }
})
instructor.bio = 'hello'
console.log(instructor.age)
console.log(instructor.sns.twitter)
</script>
<template>
  <h1>Title: {{ title }}</h1>
  <h2>Price: ${{ price - 1 }}</h2>
  <button @click="increment">button</button>
  <h2>Students: {{ info.students }}</h2>
  <h2>Instructor age: {{ instructor.age }}</h2>
  <h2>Instructor bio: {{ instructor.bio }}</h2>
  <h2>Instructor SNS Twitter: {{ instructor.sns.twitter }}</h2>
</template>
