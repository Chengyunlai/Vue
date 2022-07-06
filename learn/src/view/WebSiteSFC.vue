<template>
<!-- 第一个示例 -->
  <p>{{message}}</p>
  <button @click="changeVlaue">changeValue</button>
  <span v-html="rawHtml"></span>
</template>

<script setup>
  import { ref } from "vue";
  const message = ref('你好')
  const rawHtml = ref('<span style="color: red">This should be red.</span>')

  function changeVlaue() {
    message.value = message.value=='你好'?'hello':'你好'
  }
</script>

<style>

</style>