<template>
  <div class="flex flex-wrap justify-center">
    <div
      @click="goToPost(post.id)"
      class="w-80 m-4"
      v-for="post in posts"
      :key="post.id"
    >
      <PostListItem :item="post"></PostListItem>
    </div>
  </div>
</template>

<script>
export default {
  name: 'IndexPage',
  async asyncData ({ $content }) {
    let posts = await $content('bloggposts').sortBy('id', 'desc').without(['body']).fetch()
    console.log(posts)
    return {
      posts
    }
  },
  methods: {
    goToPost (id) {
      this.$router.push('/post-details/' + id)
    }
  }
}
</script>
