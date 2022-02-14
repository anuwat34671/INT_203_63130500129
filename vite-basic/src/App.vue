<script setup>
  const msg = "Welcome to Vue.js"
  const counter = 5;
  const headingStyle = 'color: red'
  const numStyle = 'color: blue'
  const imagePath = './images/AS002873_19.png'
  const notHTML = '<b><i>This should not be bold and italic</i></b>]'
  const hide =  true
  const depAmount = 79
  const foods = ['Steak', 'Salad', 'Tomyum', 'Fried rice']
  const students = [
    {stdId: 1234, stdName: 'Anuwat Pattanajan'},
    {stdId: 1235, stdName: 'Nutchanon Assawachin'},
    {stdId: 1236, stdName: 'Siripong Phiwkhaw'}]
  const course = {
    title: 'INT203 Client II',
    credits: 3,
    class: 'lecture & lab'
  }
</script>

<template>
  <h4 v-text="msg" v-bind:style="headingStyle"></h4>
  <p v-text="counter" v-bind:style="numStyle"></p>
  <img src="./assets/logo.png"/>
  <img v-bind:src="imagePath" alt="AS002873"/>
  <p v-show ="hide" v-text="notHTML"></p>
  <p v-show="!msg" style ="color : red">Please insert your data</p>
  <p v-if="depAmount >=80" v-text="depAmount"></p>
  <p v-else-if="depAmount >=70"> Interest : {{depAmount*5}}</p>
  <h1>Food List</h1>
  <!--v-for (array) -->
  <ul>
    <li v-for="(food, index) in foods" :key="index">{{ food }}</li>
  </ul>
  <!--v-for (array of object) -->
  <ul>
    <li v-for="student in students" :key="students.stdId">{{ student.stdName }}</li>
  </ul>
  <!--v-for (object) -->
  <ul>
    <li v-for="(propValue,propKey,index) in course">
      #{{ index }} - {{ propKey }} : {{ propValue }}
    </li>
  </ul>
</template>

<style>

</style>