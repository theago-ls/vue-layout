<template>
  <section class="card">
    <div class="post-container">
        <img class='photo' src='../assets/marketing-digital.jpg'/>
        <div class="post-text">
          <p class='title'>
            {{ title }}
          </p>
          <p class='firstParagraph'>
            {{ firstParagraph }}
          </p>
        </div>
    </div>
    <Button label='Continuar'></Button>
  </section>
</template>

<script lang="ts">
import Vue from 'vue';
import Button from './Button.vue';

export default Vue.extend({
  name: 'ConsultancyCard',
  components: {
    Button,
  },
  props: {
    title: String,
    firstParagraph: String,
  },
});
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="less">
.card {
  margin-left: 12%;
  display: flex;
  flex-direction: column;
  width: 33%;
  height: 60%;
  background: #313072;
  margin-top: 60px;
  padding: 2px;
  padding-bottom: 25px;
  text-align: left;

  .post-container{
    img {
      height: 100%;
      width: 100%;
    }

    .post-text{
      background: white;
      padding: 30px;
      margin-top: -8px;

      .title {
        font-size: 27px;
        font-weight: bold;
        color: #313072;
        line-height: 1.2;
      }

      .firstParagraph {
        margin-top: 15px;
        font-size: 18px;
        overflow: hidden;
        text-overflow: ellipsis;
        display: -webkit-box;
        -webkit-line-clamp: 3; /* number of lines to show */
        -webkit-box-orient: vertical;
      }
    }
  }

  button {
    margin-top: 30px;
  }
}

@media screen and (max-width: 968px){
  .card {
    width: 88%;
    margin-left: 4%;
  }
}

@media screen and (min-width: 1920px){
  .card {
    margin-left: 11.3%;
  }
}
</style>
