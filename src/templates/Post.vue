<template>
  <Layout>
    <div v-html="$page.post.content"/>
  </Layout>
</template>

<page-query>
query Post ($path: String!) {
  post (path: $path) {
    content
  }
}
</page-query>

<script>
  export default {}
</script>
