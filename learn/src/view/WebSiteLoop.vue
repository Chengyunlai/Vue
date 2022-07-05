<template>
  <button @click="show = !show">Toggle List</button>
  <button @click="list.push(list.length+1)">Push Number</button>
  <button @click="list.pop()">Pop Number</button>
  <button @click="list.reverse">Reverse List</button>
  <ul v-if="show && list.length" class="loop">
    <li v-for="item of list">{{item}}</li>
  </ul>
  <p v-else-if="list.length">List is Hiden</p>
  <p v-else>List is Empty!</p>
</template>

<script setup>
  import { ref } from 'vue';
  const list = ref([1, 2, 3])
  const show = ref(true)
</script>

<style>
.loop{
  color: beige;
}
</style>