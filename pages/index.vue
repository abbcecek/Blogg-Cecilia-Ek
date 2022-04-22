<template>
  <div>
    <div class="px-2 md:px-5">
      <div class="text-4xl my-8">
        <h2>Hej hej, välkommen till min blogg!</h2>
      </div>
      <div
        class="my-3 filter saturate-150 -hue-rotate-30 drop-shadow-2xl h-auto"
      >
        <img
          src="https://images.unsplash.com/photo-1526336024174-e58f5cdd8e13?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=387&q=80"
          alt="en katt med en fjäril på näsan"
          class="
            flex
            justify-center
            md:float-right
            w-full
            sm:w-2/6
            mt-2
            md:ml-2
          "
        />
      </div>
      <div class="text-xl">
        <nuxt-content class="" :document="Message"> </nuxt-content>
      </div>
      <div class="break-words w-3/5 my-10 text-xl">
        <p>
          Klicka på "inlägg" knappen högst upp på sidan för att läsa om mitt
          liv, eller så kan du klicka på "om mig" för att ta reda på lite mer om
          mig! :)
        </p>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'IndexPage',
  async asyncData ({ $content }) {
    let Message = await $content('Welcome message').fetch()

    return {
      Message
    }
  }
}
</script>