<script setup lang="ts">
import '../styles/main.css'
const showBar = ref<boolean>(true)
const isBg = ref<boolean>(false)
const spotlight = ref<HTMLInputElement>()
</script>

<template>
  <div
    class="h-fit flex m-0 space-x-4 items-center justify-center rounded-lg  px-6 py-10 w-6/12 md:w-7/12 mx-auto fixed -top-[1200px] left-1/2 transform -translate-x-1/2 -translate-y-1/2  z-[100] "
    :class="[{ 'top-1/2': showBar }, { 'transition-all duration-300 bg-violet-500 backdrop-blur-[3px] bg-opacity-5 shadow-lg': isBg }]"
  >
    <div class="shd grow rounded transition duration-150 min-h-xs bg-gray-600 border-2 border-gray-400">
      <!-- <span class="w-11/12 border-b border-gray-900" /> -->
      <input
        ref="spotlight"
        type="text"
        placeholder="Command here.."
        class="!font-semibold w-full outline-none m-0 px-3 py-2 h-15 !text-xl block  !text-gray-300  bg-transparent transition duration-150 border-b !border-white !border-opacity-30"
      >
      <!-- <hr class="!border-gray-100 opacity-40  m-auto"> -->
      <div>
        <ul class="text-gray-200">
          <li class="hover:bg-gray-100 hover:bg-opacity-10 list-none text-left transition duration-200">
            <div class="relative px-3 py-3 cursor-pointer after:content-[''] after:hidden after:w-1  after:h-full after:absolute after:top-0 after:left-0 after:bg-gray-300 hover:after:flex">
              Lo  rem, ipsum dolor sit amet consectetur
            </div>
          </li>
        </ul>
      </div>
    </div>
    <!-- <AppDial /> -->
  </div>
</template>
