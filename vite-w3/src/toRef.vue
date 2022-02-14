<script setup>
import{reactive,toRef,toRefs} from 'vue'
const cube = reactive({length:1,width:2,height:3})
const cube2 = {length:1,width:2,height:3}
const {width,height} = toRefs(cube)
console.log(width.value)
console.log(height.value)

const length = toRef(cube,'length')
console.log(length.value);
length.value = 1000
height.value = 999
console.log(cube)
console.log(cube2)
</script>

<template>
<p> {{ cube }} </p>
<p> {{ cube2 }} </p>
</template>

<style>

</style>