<template>
  <div>
    <h1>Post1</h1>
    <ul>
      <li v-for="(item, index) in posts" :key="index">
        {{item.title}}
      </li>
    </ul>
  </div>
</template>
<script>
import axios from 'axios'
export default {
  name: 'post1',
  data() {
    return {
      posts: []
    }
  },
  async created () {
    const { data } = await axios.get('https://jsonplaceholder.typicode.com/posts')
    this.posts = data
  }
}
</script>