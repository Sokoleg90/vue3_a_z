<template>
  <div class="app">

  </div>
</template>

<script>
export default {
  data() {
    return {
      posts: [
        {id: 1, title: 'JavaScript1', body: 'Description of post1'},
        {id: 2, title: 'JavaScript2', body: 'Description of post2'},
        {id: 3, title: 'JavaScript3', body: 'Description of post3'},
      ],
      title: '',
      body: '',
    }
  },

  methods: {
    createPost() {
      const newPost = {
        id: Date.now(),
        title: this.title,
        body: this.body
      }
      this.posts.push(newPost);
      this.title = '';
      this.body = '';
    },
  }
}
</script>

<style>
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

.app {
  padding: 15px;
}


</style>