<template>
  <div class='blog'>
    <BlogDelimiter>
    </BlogDelimiter>
    <div class="posts">
      <Loading :loading="loading" />
      <PostCard v-for="post in posts" :key='post.id' :title="post.title" :firstParagraph="post.body"></PostCard>
    </div>
  </div>
</template>

<script>
import BlogDelimiter from './BlogDelimiter.vue';
import Loading from './Loading.vue';
import PostCard from './PostCard.vue';

export default {
  name: 'Blog',
  props: {
    loading: Boolean,
    posts: Array,
  },
  components: {
    BlogDelimiter,
    Loading,
    PostCard,
  },
};
</script>

<style lang="less" scoped>
.blog {
  display: flex;
  flex-direction: column;
  margin-left: -20px;
  margin-top: 70px;

  .posts {
    display: flex;
    flex-direction: row;
    flex-wrap: wrap;
  }
}

@media screen and (max-width: 968px) {
  .blog {
    flex-direction: column;

    .posts {
      flex-direction: column;
      align-items: center;
    }
  }
}
</style>
