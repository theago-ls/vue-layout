<template>
  <div id="app">
    <ConsultancyCard>
    </ConsultancyCard>
    <FormCard>
    </FormCard>
  </div>
</template>

<script lang="ts">
import Vue from 'vue';
import ConsultancyCard from './components/ConsultancyCard.vue';
import FormCard from './components/FormCard.vue';

export default Vue.extend({
  name: 'App',
  components: {
    ConsultancyCard,
    FormCard,
  },
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
  justify-content: center;
  height: 100%;
  width: 100%;
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  padding: 21% 20px;
  background-image: url('./assets/family-background.jpg');
  background-size: 100%;
  background-repeat: no-repeat;
  background-position: 0 0;
}
</style>
