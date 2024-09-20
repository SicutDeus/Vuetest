<script>


export default {
  data(){
    return {
      post: {
        title:'',
        body: ''
      }
    }
  },
  methods: {
    createPost() {
      this.post.id = Date.now()
      this.$emit('create', this.post)

      this.post = {
        'title': '',
        'body': '',
      }
  }
  }
}
</script>

<template>
  <div>
    <div class="app">
      <form @submit.prevent>
        <h4>Создание поста</h4>
        <my-input class="input" v-model="post.title" type="text" placeholder="Название" />
        <my-input class="input" v-model="post.body" type="text" placeholder="Описание" />
        <my-button
          @click="createPost"
          style="align-self: flex-end; margin-top: 20px"
        >Создать</my-button>
      </form>
    </div>
  </div>
</template>

<style scoped>

.app {
  padding: 20px;
}

form {
  display: flex;
  flex-direction: column;
}
</style>