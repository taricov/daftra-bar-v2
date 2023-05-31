<script setup lang="ts">
const showBar = ref<boolean>(true)
const isBg = ref<boolean>(false)
const spotlight = ref<HTMLInputElement>()
</script>

<template>
  <div
    class="h-fit flex items-center justify-center rounded-lg shadow-lg px-6 py-10  w-6/12 mx-auto fixed -top-[1200px] left-1/2 transform -translate-x-1/2 -translate-y-1/2  z-[100] transition-all duration-300"
    :class="[{ 'top-1/2': showBar }, { 'bg-violet-500 backdrop-blur-[3px] bg-opacity-5': isBg }]"
  >
    <input
      id="spotlight"
      ref="spotlight"
      type="text"
      placeholder="Spotlight-Search"
      class="shadow-xl rounded px-3 py-2 block h-12 m-auto text-2xl text-black bg-red-100 bg-no-repeat"
    >
    <AppDial />
  </div>
</template>
