<script setup>
import HelloWorld from './components/HelloWorld.vue'
import TheWelcome from './components/TheWelcome.vue'
import WebSiteSFC from './view/WebSiteSFC.vue';
import WebSiteInput from './view/WebSiteInput.vue';
import WebSiteAttribute from './view/WebSiteAttribute.vue';
import WebSiteLoop from './view/WebSiteLoop.vue';
import WebSiteCompoent from './view/WebSiteCompoent.vue';
import Markdown from './view/Markdown.vue';

</script>

<template>
  <header>

    <img alt="Vue logo" class="logo" src="./assets/logo.svg" width="125" height="125" />

    <div class="wrapper">
      <HelloWorld msg="Hello World!" />
    </div>
  </header>

  <main>
    <TheWelcome />

  </main>
  <h1 class='demo'>DEMO SHOW</h1>
  <br>
  <WebSiteSFC></WebSiteSFC>
  <WebSiteInput></WebSiteInput>
  <WebSiteAttribute></WebSiteAttribute>
  <WebSiteLoop></WebSiteLoop>
  <WebSiteCompoent></WebSiteCompoent>
  <Markdown></Markdown>
</template>

<style>
@import './assets/base.css';

.demo{
  color: aquamarine;
}

#app {
  max-width: 1280px;
  margin: 0 auto;
  padding: 2rem;

  font-weight: normal;
}

header {
  line-height: 1.5;
}

.logo {
  display: block;
  margin: 0 auto 2rem;
}

a,
.green {
  text-decoration: none;
  color: hsla(160, 100%, 37%, 1);
  transition: 0.4s;
}

@media (hover: hover) {
  a:hover {
    background-color: hsla(160, 100%, 37%, 0.2);
  }
}

@media (min-width: 1024px) {
  body {
    display: flex;
    place-items: center;
  }

  #app {
    display: grid;
    grid-template-columns: 1fr 1fr;
    padding: 0 2rem;
  }

  header {
    display: flex;
    place-items: center;
    padding-right: calc(var(--section-gap) / 2);
  }

  header .wrapper {
    display: flex;
    place-items: flex-start;
    flex-wrap: wrap;
  }

  .logo {
    margin: 0 2rem 0 0;
  }
}
</style>
