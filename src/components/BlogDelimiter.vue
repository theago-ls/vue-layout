<template>
  <section class="card">
    <p class='title'>Pense nisso...</p>
    <p class='subtitle'>
        O quanto o diagnóstico de uma doença grave,
         internação ou cirurgia inesperada pode afetar,
         hoje, sua vida pessoal e financeira?
    </p>

    <span class='blog-tile'>Blog</span>
  </section>
</template>

<script lang="ts">
import Vue from 'vue';

export default Vue.extend({
  name: 'BlogDelimiter',
});
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="less">
.card {
  display: flex;
  flex-direction: column;
  width: 44%;
  text-align: left;

  p {
    color: #313072;
    font-size: 30px;
  }

  .title {
    font-size: 38px;
    font-weight: bold;
    color: #ff9b23;
    margin-left: 30%;
  }

  .subtitle {
    font-size: 22px;
    text-align: justify;
    margin: 20px 0;
    margin-left: 30%;
  }

  .blog-tile {
    font-size: 64px;
    color: white;
    background-color: #313072;
    padding-left: 48%;
  }
}
</style>
