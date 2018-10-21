<template>
  <Layout>
    <div>
      <h2>Blog Posts</h2>
      <div v-for="item in $page.allPost.edges">
        <g-link :to="item.node.path">{{ item.node.title }}</g-link>
      </div>
    </div>
    <g-image alt="Example image" src="~/favicon.png" width="135" />
    <h1>Hello, world!</h1>
    <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Pariatur excepturi labore tempore expedita, et iste tenetur suscipit explicabo! Dolores, aperiam non officia eos quod asperiores</p>
  </Layout>
</template>

<page-query>
query posts {
  allPost{
    edges {
      node {
        path
        title
      }
    }
  }
}
</page-query>

<script>
export default {}
</script>
