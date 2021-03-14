<template>
  <div id="app">
    <div class='top-cards'>
      <ConsultancyCard>
      </ConsultancyCard>
      <FormCard>
      </FormCard>
    </div>
    <Blog :loading="loading" :posts="posts"/>
  </div>
</template>

<script lang="ts">
import Vue from 'vue';
import ConsultancyCard from './components/ConsultancyCard.vue';
import FormCard from './components/FormCard.vue';
import Blog from './components/Blog.vue';

export default Vue.extend({
  name: 'App',
  components: {
    ConsultancyCard,
    FormCard,
    Blog,
  },
  data: () => ({
    loading: false,
    posts: null,
  }),
  created() {
    this.fetchPosts();
  },
  methods: {
    fetchPosts() {
      this.loading = true;

      fetch('http://jsonplaceholder.typicode.com/posts').then((res) => res.json()).then((posts) => {
        this.posts = posts;
        this.loading = false;
      });
    },
  },
});
</script>

<style lang="less">
* {
  padding: 0;
  margin: 0;
}

body {
  width: 100vw;
  height: 100%;
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
  padding-bottom: 5%;
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

@media screen and (max-width: 968px) {
  #app {
    background-size: 120%;
    background-position: 10% 0;
    padding: 19% 0px;
  }

  .top-cards {
    flex-direction: column;
    align-items: center;
  }
}
</style>
