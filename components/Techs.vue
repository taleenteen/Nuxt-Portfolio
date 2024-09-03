<script setup>
const images = [
  "/html.png",
  "/css.png",
  "/js.png",
  "/vue.png",
  "/react.png",
  "/nuxtjs.png",
  "/nextjs.png",
  "/tailwind.png",
  "/vscode.png",
  "/github.png",
];
</script>

<template>
  <div class="max-w-screen-xl mx-auto py-8 px-4 lg:py-16 lg:px-6">
    <div class="flex flex-col items-center">
      <h1 class="text-center text-3xl font-bold">My Tech Stack</h1>
      <h2 class="text-center text-xl mt-4">
        Technologies I've been working with recently
      </h2>
    </div>
    <div class="avatar flex flex-wrap justify-center drop-shadow-2xl">
      <div
        v-for="(image, index) in images"
        :key="index"
        class="w-[150px] md:w-1/5 p-4 md:p-8 lg:p-16"
      >
        <img :src="image" class="w-24 max-w-full mx-auto" />
      </div>
    </div>
  </div>
</template>
