<script setup>
import { ref } from 'vue'

const suggestion = ref('')
const favorcolor = ref('')
const agree = ref(false)
const jobs = ref([])
const food = ref('')
const activities = ref([])
</script>
 
<template>
<div>
Suggestion &nbsp;
<textarea v-model = "suggestion" cols="40" rows="5" placeholder="Enter your answer here...."></textarea>
<p> {{ suggestion}} </p>
</div>
<div>
    <input type="radio" value="Red" v-model="favorcolor" /><label> Red </label>
    <input type="radio" value="Green" v-model="favorcolor" /><label> Green </label>
    <input type="radio" value="Blue" v-model="favorcolor"><label> Blue </label>
    <p> {{favorcolor}} </p>
</div>
<div>
    <input type="checkbox" v-model = "agree"><label> I agree </label>
    <p> {{agree}} </p>
</div>
<div>
    <input type="checkbox" value="Front-End" v-model="jobs"><label> front-end </label>
    <input type="checkbox" value="Back-End" v-model="jobs"><label> Back-end </label>
    <input type="checkbox" value="Dev-Ops" v-model="jobs"><label> Dev-Ops </label>
    <p> {{jobs}} </p>
</div>
<div>
    <select v-model="food">
        <option value="PIZZA"> Pizza </option>
        <option value="SOUP"> Soup </option>
        <option value="PASTA"> Pasta </option>
        <option value="HAMBURGER"> Hamburger </option>
    </select>
    <p> {{food}} </p>
</div>
<div>
    <select v-model="activities" multiple>
        <option value="WALK"> Walk </option>
        <option value="RUN"> Run </option>
        <option value="SIT"> Sit </option>
        <option value="SLEEP"> Sleep </option>
    </select>
    <p> {{activities}} </p>
</div>
</template>
 
<style>

</style>