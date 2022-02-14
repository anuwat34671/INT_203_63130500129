<script setup>

const warningColor = "red"
const warningStyle = "italic"
const successText = "color:green"
const decorText = "text-decoration:underline"
const isEmpty = false
const hasDecor = true
const isSucceed = false
const errorStyle = 'error-text'
const decorStyle = 'decor-text'
</script>

<template>
  <div>
    <!-- binding style (object syntax) -->
    <p :style="{ color: warningColor, 'font-style': warningStyle }">
      This is a warning text.
    </p>
    <p :style="isEmpty ? { color: 'red' } : { color: 'green' }">
      This is a style under condition
    </p>
    <!-- binding style (array syntax) -->
    <p :style="[successText]">This is a success text</p>
    <p :style="[successText, decorText]">This is success and decoration text</p>
    <p :style="[successText, hasDecor ? decorText : '']">
      This is styles under condition
    </p>
</div>
<div>
    <!-- class attribute with object syntax -->
    <p :class="{ 'success-text': isSucceed }">
      this applied success-text class
    </p>
    <p :class="{ 'success-text': isSucceed, 'decor-text': hasDecor }">
      this applied success-text and class
    </p>
</div>
<div>
    <!-- class attribute with object syntax -->
    <p :class="{ 'success-text': isSucceed }">
      this applied success-text class
    </p>
    <p :class="{ 'success-text': isSucceed, 'decor-text': hasDecor }">
      this applied success-text and class
    </p>
    <!-- class attribute with array syntax -->
    <p :class="[errorStyle, decorStyle]">
      This applied style stored in variable
    </p>
    <p :class="isSucceed ? 'success-text' : 'error-text'">
      This applied style under condition
    </p>
    <p :class="['decor-text', isSucceed ? 'success-text' : 'error-text']">
      Lorem ipsum dolor sit amet consectetur adipisicing elit. Dolor quia amet
      aspernatur, quo inventore autem consequatur incidunt. Laudantium minus
      ipsam obcaecati dolorum deleniti reiciendis quibusdam architecto totam
      voluptatem incidunt! Voluptas!
    </p>
</div>

</template>

<style>
.success-text { color: green; }
.error-text { color: red; font-style:italic; }
.warning-text { color: orange;}
</style>