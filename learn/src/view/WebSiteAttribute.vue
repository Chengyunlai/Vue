<template>
<!-- 这是v-bind的一种用法，简写是: -->
  <p :title="title">
    Hover your mouse over me for a few seconds to see my dynamically bound
    title!
  </p>
  <p :class="{red : isRed}" @click="toggleRed">This should be red... but click me to toggle it.</p>
  <p :style="{color}" @click="toggleColor">
    This should be green, and should toggle between green and blue on click.
  </p>
</template>

<script setup>

import { ref } from "vue";
const title = ref("hello ~");
const isRed = ref(true)
const color = ref('green')

function toggleRed(){
  isRed.value = !isRed.value;
}

function toggleColor(){
  color.value = color.value === 'green'?'blue':'green';
}

</script>


<style>
.red{
  color: red;
}
</style>
