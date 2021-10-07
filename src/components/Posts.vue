<template>
  <div>
    <h1>Posts</h1>
    <ul>
      <li v-for="post in posts" :key="post.id">
        {{ post.title }}
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  data() {
    return {
      posts: [],
    }
  },
  created: function () {
    this.fetchData()
  },
  methods: {
    fetchData: async function () {
      try {
        const res = await fetch("https://jsonplaceholder.typicode.com/posts")
        const posts = await res.json()
        this.posts = posts
      } catch (error) {
        console.log(error)
      }
    },
  },
}
</script>

<style scoped></style>
