<template>
  <div class="w-full mx-auto bg-white p-3">
    <!-- <div class="w-128">
      <div
        class="bg-fixed bg-contain bg-no-repeat h-64"
        v-bind:style="{ backgroundImage: 'url(' + post.image + ')' }"
      ></div>
    </div> -->
    <div class="w-full flex justify-center">
      <img
        class="
          w-full
          object-cover
          border-8 border-red-200 border-dashed
          rounded-3xl
        "
        :src="post.image"
      />
    </div>
    <div class="">
      <div class="flex justify-center">
        <h1 class="text-2xl md:text-7xl mb-4 underline mt-4">
          {{ post.title }}
        </h1>
      </div>
      <div class="mx-2 md:mx-5">
        <p class="mb-8 text-lg md:text-4xl">{{ post.description }}</p>
        <div class="w-full break-words text-md md:text-xl">
          <nuxt-content class="mb-10" :document="post"></nuxt-content>
        </div>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  async asyncData ({ $content, params }) {

    let post = await $content('bloggposts/post' + params.id).fetch()
    console.log(post)

    return {
      post
    }
  },
}
</script>