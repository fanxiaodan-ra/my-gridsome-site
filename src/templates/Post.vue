<template>
  <div>
    <h1>{{$page.post.title}}</h1>
    <p>{{$page.post.body}}</p>
  </div>
</template>
<page-query>
  query($id: ID!) {
    post (id: $id) {
      id
      title
      body
    }
  }
</page-query>
<script>
export default {
  metaInfo() {
    return {
      title: this.$page.post.title
    }
  }
}
</script>