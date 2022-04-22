<template>
  <div>
    <nuxt-content :document="markdown" class="my-10 px-5 text-xl md:text-2xl">
    </nuxt-content>
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