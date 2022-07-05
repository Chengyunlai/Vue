<template>
<!-- 第一个示例 -->
  <p>{{message}}</p>
  <button @click="changeVlaue">changeValue</button>
</template>

<script setup>
  import { ref } from "vue";
  const message = ref('你好')

  function changeVlaue() {
    message.value = message.value=='你好'?'hello':'你好'
  }
</script>

<style>

</style>