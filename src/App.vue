<template>
  <div id="app">
    <div class='top-cards'>
      <ConsultancyCard>
      </ConsultancyCard>
      <FormCard>
      </FormCard>
    </div>
    <div class='blog'>
      <BlogDelimiter>
      </BlogDelimiter>
      <div class="posts">
        <PostCard></PostCard>
        <PostCard></PostCard>
      </div>
    </div>
  </div>
</template>

<script lang="ts">
import Vue from 'vue';
import ConsultancyCard from './components/ConsultancyCard.vue';
import FormCard from './components/FormCard.vue';
import BlogDelimiter from './components/BlogDelimiter.vue';
import PostCard from './components/PostCard.vue';

export default Vue.extend({
  name: 'App',
  components: {
    ConsultancyCard,
    FormCard,
    BlogDelimiter,
    PostCard,
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
  flex-direction: column;
  height: 100%;
  width: 100%;
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  padding: 19% 20px;
  background-image: url('./assets/family-background.jpg');
  background-size: 100%;
  background-repeat: no-repeat;
  background-position: 0 0;
}

.top-cards {
  display: flex;
  flex-direction: row;
  justify-content: center;
}

.blog {
  display: flex;
  flex-direction: column;
  margin-left: -20px;
  margin-top: 70px;

  .posts {
    display: flex;
  }
}
</style>
