<template>
  <div id="app">
  </div>
</template>

<script lang="ts">
import Vue from 'vue';
import Card from './components/Card.vue';

export default Vue.extend({
  name: 'App',
});
</script>

<style lang="less">
* {
  padding:0;
  margin:0;
}

body {
  width: 100vw;
  height: 100vh;
}

#app {
  display: flex;
  height: 100%;
  width: 100%;
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  padding: 30px 20px;
  background-image: url('./assets/family-background.jpg');
  background-size: 100%;
  background-repeat: no-repeat;
  background-position: 0 -500px;
}
</style>
