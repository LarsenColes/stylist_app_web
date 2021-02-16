<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png" />
    <Home />
  </div>
</template>

<script>
import Home from './pages/Home.vue';
import './assets/tailwind.css';
export default {
  name: 'App',
  components: {
    Home,
  },
};
</script>

<style></style>
