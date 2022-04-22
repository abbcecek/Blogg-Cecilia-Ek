<template>
  <div
    class="
      bg-red-100
      rounded-3xl
      pb-10
      transform
      transition
      duration-500
      ease-in-out
      hover:scale-105
      border-8 border-red-200 border-dashed
    "
  >
    <img
      :src="item.image"
      alt="post image"
      class="h-80 w-full object-cover rounded-2xl border-red-200"
    />
    <div class="px-3">
      <h3 class="font-bold text-2xl">{{ item.title }}</h3>
      <p class="text-md italic">{{ item.date }}</p>
      <p class="text-lg">{{ item.description }}</p>
    </div>
  </div>
</template>

<script>
export default {
  props: ['item'],
  data () {
    return {

    }
  }
}
</script>