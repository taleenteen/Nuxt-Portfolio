<script setup>
const title = "For any questions please mail us :";
const email = "teenpanuvit@gmail.com";

function copyEmail() {
  const tempInput = document.createElement("input");
  tempInput.value = email;
  document.body.appendChild(tempInput);

  tempInput.select();
  tempInput.setSelectionRange(0, 99999);

  document.execCommand("copy");

  document.body.removeChild(tempInput);

  alert("Email copied to clipboard: " + email);
}
</script>

<template>
  <div
    class="hero min-h-screen flex items-center justify-center px-4 sm:px-6 lg:px-8"
  >
    <div class="hero-content text-center overflow-visible">
      <div class="max-w-xl mx-auto">
        <h1
          class="text-3xl sm:text-4xl md:text-5xl font-bold bg-gradient-to-r from-pink-300 via-blue-500 to-green-400 text-transparent bg-clip-text bg-300% animate-gradient leading-relaxed"
        >
          {{ title }}
        </h1>
        <h1
          class="text-3xl sm:text-4xl md:text-5xl font-semibold text-gray-900"
        >
          {{ email }}
        </h1>

        <button class="btn btn-outline mt-8 md:mt-12" @click="copyEmail">
          <svg
            xmlns="http://www.w3.org/2000/svg"
            fill="none"
            viewBox="0 0 24 24"
            stroke-width="1.5"
            stroke="currentColor"
            class="w-6 h-6"
          >
            <path
              stroke-linecap="round"
              stroke-linejoin="round"
              d="M15.666 3.888A2.25 2.25 0 0 0 13.5 2.25h-3c-1.03 0-1.9.693-2.166 1.638m7.332 0c.055.194.084.4.084.612v0a.75.75 0 0 1-.75.75H9a.75.75 0 0 1-.75-.75v0c0-.212.03-.418.084-.612m7.332 0c.646.049 1.288.11 1.927.184 1.1.128 1.907 1.077 1.907 2.185V19.5a2.25 2.25 0 0 1-2.25 2.25H6.75A2.25 2.25 0 0 1 4.5 19.5V6.257c0-1.108.806-2.057 1.907-2.185a48.208 48.208 0 0 1 1.927-.184"
            />
          </svg>
          Copy My Email
        </button>
      </div>
    </div>
  </div>
</template>
