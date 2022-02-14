<script setup>
import { reactive } from 'vue'
const product = reactive({})
const course = reactive(['INT201','INT202','INT203'])
product.name = 'computer'
product.price = 1500
console.log(product)
console.log(product.name)

let myArray = ['value1','value2','value3']
let mySet = reactive(new Set(myArray))
console.log(mySet)

const map1 = new Map()
map1.set('a',1)
map1.set('b',2)
map1.set('c',3)
map1.set('d',4)
map1.set('e',5)

console.log(map1)
const myMap = reactive(map1)
console.log(myMap);
setTimeout(() => { myMap.set('z', 100)})

const map2 = new Map()
map2.set('good', 10)
map2.set('fair', 5)

setTimeout(() => {
  map2.set('poor', 1)
  console.log(map2)
}, 1000)
</script>
 
<template>
    <p>{{ product }}</p>
    <p>{{ product.price }}</p>
    <p> My Map: {{ myMap }}</p>
    <p> Map2: {{ map2 }}</p>
</template>
 
<style>

</style>