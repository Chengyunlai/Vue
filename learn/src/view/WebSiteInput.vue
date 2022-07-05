<template>
<!-- 第二个示例 -->
  <h1>{{ message }}</h1>
  <button @click="reverseMessage">reverse</button>
  <button @click="message += '!'">append！</button>
  <!--阻止网页刷新-->
  <a href="https://vuejs.org" @click.prevent="notify">
    A link with e.preventDefault()
  </a>
</template>

<script setup>
import { ref } from "vue";
const message = ref("Hello!");

function reverseMessage() {
  message.value = message.value.split("").reverse().join("");
}

function notify() {
  alert("stop it !");
}
</script>

<style lang=""></style>
