<template>
  <div
    class="
      font-sans
      bg-red-300
      h-auto
      text-white
      p-4
      mb-5
      rounded-t-3xl
      text-center
      border-b-8 border-double border-white
    "
  >
    <h1 class="m-3 font-mono text-3xl xl:text font-bold">Blogg</h1>
    <div class="flex justify-around content-start">
      <nuxt-link
        to="/"
        class="
          w-16
          mx-3
          p-1
          mb-3
          inline-block
          hover:bg-red-200
          focus:outline-none focus:ring focus:ring-red-00
          rounded-2xl
          hidden
          md:inline-block
          cursor-pointer
          transform
          transition
          duration-500
          ease-in-out
          hover:scale-110
        "
        tag="img"
        src="https://naturuppdraget.se/icons/specialuppdrag-hjarta.png"
      ></nuxt-link>

      <div class="flex justify-center text-sm md:text-xl">
        <nuxt-link
          to="/"
          class="
            border-4 border-red-200 border-double
            md:bg-red-300
            md:border-transparent
            md:bg-opacity-75
            md:hover:bg-red-200
            md:hover:tracking-widest
            focus:outline-none focus:ring focus:ring-red-100
            rounded-lg
            py-1
            px-4
            m-2
            h-10
            transform
            transition
            duration-500
            ease-in-out
            hover:scale-110
          "
          >Startsida</nuxt-link
        >
        <nuxt-link
          to="/posts"
          class="
            border-4 border-red-200 border-double
            md:bg-red-300
            md:border-transparent
            md:bg-opacity-75
            md:hover:bg-red-200
            md:hover:tracking-widest
            focus:outline-none focus:ring focus:ring-red-100
            rounded-lg
            py-1
            px-4
            m-2
            h-10
            transform
            transition
            duration-500
            ease-in-out
            hover:scale-110
          "
          >Inlägg</nuxt-link
        >
        <nuxt-link
          to="/om-mig"
          class="
            border-4 border-red-200 border-double
            md:bg-red-300
            md:border-transparent
            md:bg-opacity-75
            md:hover:bg-red-200
            md:hover:tracking-widest
            focus:outline-none focus:ring focus:ring-red-100
            rounded-lg
            py-1
            px-4
            m-2
            h-10
            transform
            transition
            duration-500
            ease-in-out
            hover:scale-110
          "
          >Om mig</nuxt-link
        >
      </div>
      <div class="w-20 my-0 mx-3 hidden md:inline-block"></div>
    </div>
  </div>
</template>