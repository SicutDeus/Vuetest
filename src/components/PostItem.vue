<script>

export default {
  props: {
      post: {
        type: Object,
        required: true
      }
  }
}
</script>

<template>
  <div class="post">
    <div>
      <div><strong>Название: </strong> {{ post.title }}</div>
      <div><strong>Описание: </strong> {{ post.body }}</div>
    </div>
    <div class="post_btns">
      <my-button>Удалить</my-button>
    </div>
  </div>
</template>

<style scoped>
.post {
  padding: 15px;
  border: 2px solid teal;
  margin-top: 15px;
  margin-left: 20px;
  margin-right: 20px;
  display: flex;
  align-items: center;
  justify-content: space-between;
}
</style>