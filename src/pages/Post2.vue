<template>
  <div>
    <h1>Post2</h1>
    <ul>
      <li v-for="(edge, index) in $page.posts.edges" :key="index">
        <g-link :to="edge.node.path">{{edge.node.title}}</g-link>
      </li>
    </ul>
  </div>
</template>

<page-query>
  query{
    posts: allPost {
      edges {
        node{
          id
          title
          body
          path
        }
      }
    }
  }
</page-query>
