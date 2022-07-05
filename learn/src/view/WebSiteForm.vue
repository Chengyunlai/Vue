<template>
  <h1>Text Input</h1>
  <input type="text" v-model="message">{{message}}
  <h1>CheckBox</h1>
  <input type="checkbox" id="checkcheck" v-model="checked">
  <label for="checkcheck">{{checked}}</label>
  <h1>Multi Checkbox</h1>

  <br/>
  <input type="checkbox" id="jack" value="Jack" v-model="checkedNames">
  <label for="jack">Jack</label>
  <input type="checkbox" id="john" value="John" v-model="checkedNames">
  <label for="john">John</label>
  <input type="checkbox" id="mike" value="Mike" v-model="checkedNames">
  <label for="mike">Mike</label>
  <p>Checked names: <pre>{{ checkedNames }}</pre></p>

  <h1>Radio</h1>
  <input type="radio" id="one" value="One" v-model="picked">
  <label for="one">One</label>
  <br>
  <input type="radio" id="two" value="Two" v-model="picked">
  <label for="two">Two</label>
  <br>
  <span>Picked: {{ picked }}</span>

  <h2>Select</h2>
  <select v-model="selected">
    <option disabled value="">Please select one</option>
    <option>A</option>
    <option>B</option>
    <option>C</option>
  </select>
  <span>Selected: {{ selected }}</span>

  <h2>Multi Select</h2>
  <select v-model="multiSelected" multiple style="width:100px">
    <option>A</option>
    <option>B</option>
    <option>C</option>
  </select>
  <span>Selected: {{ multiSelected }}</span>

</template>

<script setup>
import { ref } from 'vue';
const message = ref('Edit me')
const checked = ref(true)
const checkedNames = ref(['Jack'])
const picked = ref("One")
const selected = ref("A")
const multiSelected = ref("A")
</script>

<style>

</style>