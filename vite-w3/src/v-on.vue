<script setup>
import { ref, computed } from "vue"
console.clear()
const base = ref(2)
const height = ref(2)
const area = computed(() => {
  return ( 1 / 2 ) * base.value * height.value
})
</script>


<template>
  <p>Base: {{ base }}</p>
  <button @click="++base">Add 1 to Base</button> &nbsp;
  <button @click="--base">Subtract 1 from Base</button> &nbsp;
  <button @click="++height">Add 1 to Height</button> &nbsp;
  <button @click="--height">Subtract 1 from Height</button> &nbsp;
  <p>Height : {{ height }}</p> 
  <p>Result Area: {{ area }}</p>
</template>

<style></style>