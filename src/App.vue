<template>
<div class = "app">
  <post-form
    @create="createPost"
  />
  <post-list
    :posts="posts"
/>
</div>
</template>

<script>
import PostForm from '@/components/PostForm.vue'
import PostList from '@/components/PostList.vue'
export default {
  components: {
    PostList, PostForm
  },
  data() {
    return {
      posts: [
        { id: 1, title: 'JavaScript', body: 'JavaScript  описание 1' },
        { id: 2, title: 'JavaScript2', body: 'JavaScript  описание 2' },
        { id: 3, title: 'JavaScript3', body: 'JavaScript  описание 3' }
      ],
    }
  },
  methods: {
  createPost(post) {
    this.posts.push(post)
  }
  }
}
</script>

<style>
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}
</style>
