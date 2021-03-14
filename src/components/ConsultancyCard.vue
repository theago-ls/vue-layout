<template>
  <section class="card">
    <p class='topSubtitle'>Vida toda</p>
    <p class='title-top'>BEM</p>
    <p class='title-bottom'>ESTAR</p>
    <p class='subtitle'>Soluções completas para viver mais e melhor</p>

    <button>
      Quero uma consultoria
    </button>
  </section>
</template>

<script lang="ts">
import Vue from 'vue';

export default Vue.extend({
  name: 'ConsultancyCard',
});
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="less">
.card {
  display: flex;
  flex-direction: column;
  width: 30%;
  border: 4px solid #313072;
  padding: 25px 15px;
  text-align: left;

  p {
    color: #313072;
    font-size: 30px;
  }

  .topSubtitle {
    margin-bottom: -35px;
    margin-left: 8px;
  }

  .title-top, .title-bottom {
    font-size: 138px;
    font-weight: bold;
  }

  .title-bottom {
    margin-top: -20px;
  }

  .subtitle {
    font-size: 38px;
    margin: 80px 0;
  }

  button {
    display: flex;
    place-content: center;
    align-self: center;
    font-size: 26px;
    padding: 20px;
    color: white;
    background-color: #ff9b23;
    border: none;
    width: 95%;
  }
}
</style>
