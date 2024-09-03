<template>
  <div class="max-w-screen-xl mx-auto py-8 px-4 lg:py-16 lg:px-6">
    <div
      class="flex flex-col md:flex-row justify-center md:justify-between items-center w-full"
    >
      <div class="px-2 py-12 w-full md:w-auto md:flex-1">
        <h1
          class="text-5xl font-bold bg-gradient-to-r from-pink-300 via-blue-500 to-green-400 text-transparent bg-clip-text bg-300% animate-gradient mt-16 leading-relaxed"
        >
          Hi <span class="text-black">&#128075;</span><span>&#44;</span><br />
          My name is <br />
          Panuvit <br />
          I am a front-end developer
        </h1>
      </div>

      <div class="px-2 py-12 w-full md:w-auto flex justify-center">
        <div class="avatar">
          <div
            class="relative w-80 h-80 rounded-full p-1 bg-gradient-to-r from-pink-300 via-blue-500 to-green-400 overflow-hidden animate-gradient bg-300%"
          >
            <div class="w-full h-full rounded-full bg-white p-1">
              <img
                src="/me.jpg"
                class="object-cover w-full h-full rounded-full z-10"
              />
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>
