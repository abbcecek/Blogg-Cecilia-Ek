<template>
  <div>
    <nuxt-content :document="markdown" class="my-4 p-5 text-xl"> </nuxt-content>
  </div>
</template>

<script>
export default {
  name: 'IndexPage',
  async asyncData ({ $content }) {
    let markdown = await $content('AboutMe').fetch()

    return {
      markdown
    }
  }
}
</script>