<script setup>
const projects = [
  {
    title: "Blog News",
    picture: "/Projects/News.png",
    details:
      "Handled the frontend by creating the structure and designing the UX/UI, drawing inspiration from other websites. Also created middleware files in the Nuxt project to check user states and connect APIs to the backend server.",
    tools: "Html, JavaScript, Nuxt 2, Vuetify",
    code: `https://github.com/taleenteen/News-blog-by-Nuxt2`,
  },
  {
    title: "Game Server Site",
    picture: "/Projects/Fivem2.png",
    details:
      "Worked on an intern project, where I waited for the design team to complete their designs and then implemented them using company-provided themes.",
    tools: "Html, JavaScript, Nuxt 2, Vuetify, Figma",
  },
  {
    title: "Booking & Managing",
    picture: "/Projects/Fppp.png",
    details:
      "Worked on real-world projects, designed UX/UI, created smart admin tables for editing information on the website, connected APIs to the backend, and spent some time experimenting with backend coding using Express.",
    tools: "Html, JavaScript, Nuxt 2, Vuetify, Figma, Express",
    code: `https://github.com/panwazii/FPPP-RSU`,
    link: `https://pilotplant.rsu.ac.th`,
  },
  {
    title: "Landing Page",
    picture: "/Projects/kpcx.png",
    details:
      "Create a landing page site for a company that wants to showcase the benefits of their brand, developed with a design provided by the client.",
    tools: "Html, TypeScript, NextJs 14, TailwindCss",
    code: `https://github.com/taleenteen/kpcx-project`,
    link: `https://kpcx-project-beta.vercel.app/`,
  },
];
</script>

<template>
  <div class="max-w-screen-xl mx-auto py-8 px-4 lg:py-16 lg:px-6">
    <div class="flex flex-col items-center">
      <h1 class="text-center text-3xl font-bold">Projects</h1>
      <h2 class="text-center text-xl mt-4">Things I've built so far</h2>
    </div>

    <div
      class="grid grid-cols-1 sm:grid-cols-2 md:grid-cols-2 lg:grid-cols-4 gap-4 mt-6"
    >
      <div
        v-for="(project, index) in projects"
        :key="index"
        class="card rounded-2xl overflow-hidden shadow-xl"
      >
        <figure>
          <img
            :src="project.picture"
            alt="Project Image"
            class="h-[270px] w-full object-cover"
          />
        </figure>
        <div class="card-body p-4">
          <h3 class="text-lg font-bold">{{ project.title }}</h3>
          <p class="text-lg text-gray-700">{{ project.details }}</p>
          <h3 class="text-lg font-semibold text-green-500">
            Tech Stack:
            <span class="text-md font-normal text-gray-500">{{
              project.tools
            }}</span>
          </h3>

          <ul class="flex justify-between font-semibold">
            <li v-if="project.link" class="group">
              <a :href="project.link" target="_blank" rel="noopener noreferrer"
                >Link Preview</a
              >
              <span
                class="block max-w-0 group-hover:max-w-full transition-all duration-500 h-0.5 bg-blue-300"
              ></span>
            </li>
            <li v-else class="text-gray-500 cursor-not-allowed">
              Not Available
            </li>

            <li v-if="project.code" class="group">
              <a :href="project.code" target="_blank" rel="noopener noreferrer"
                >View Code</a
              >
              <span
                class="block max-w-0 group-hover:max-w-full transition-all duration-500 h-0.5 bg-blue-300"
              ></span>
            </li>
            <li v-else class="text-gray-500 cursor-not-allowed">
              Not Available
            </li>
          </ul>
        </div>
      </div>
    </div>
  </div>
</template>
