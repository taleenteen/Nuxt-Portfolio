<script setup>
const AboutInfo = `
My name is Panuvit Khaoikham, but you can call me Teen. I am a recent graduate from Rangsit University with a degree in Computer Science (DIT). I have experience working as a frontend web developer.`;
const WorkInfo = [
  {
    Role: "Front end Developer Intern",
    Place: "Khon Kaen",
    CompanyName: "Grit consultant",
    Duration: "2021-2022",
    Status: "Internship",
  },
  {
    Role: "Web Developer Freelance",
    Place: "Bangkok",
    CompanyName: "Clients",
    Duration: "2024",
    Status: "Freelance",
  },
];

const EducationInfo = [
  {
    Title: "Bachelor in Computer Science",
    Location: "Rangsit University",
    Status: "Full Time",
    Duration: "2019-2024",
  },
];
</script>

<template>
  <div class="max-w-screen-xl mx-auto py-8 px-4 lg:py-16 lg:px-6">
    <div class="flex flex-col">
      <h1 class="text-3xl font-bold">About Me</h1>
      <div>
        <p class="text-lg my-12">
          {{ AboutInfo }}
        </p>
      </div>
    </div>

    <div class="flex flex-col">
      <h1 class="text-3xl font-bold mb-6">Work Experience</h1>
      <div v-for="(experience, index) in WorkInfo" :key="index">
        <div class="flex justify-between items-center my-5">
          <h1 class="text-2xl">{{ experience.Role }}</h1>
          <div class="bg-green-200 px-8 py-2 rounded-full">
            <h3 class="text-green-700 font-bold">
              {{ experience.Status }}
            </h3>
          </div>
        </div>
        <div class="flex justify-between flex-wrap items-center my-5">
          <h1 class="text-lg flex items-center">
            <span class="inline-flex align-middle mr-2">
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
                  d="M3.75 21h16.5M4.5 3h15M5.25 3v18m13.5-18v18M9 6.75h1.5m-1.5 3h1.5m-1.5 3h1.5m3-6H15m-1.5 3H15m-1.5 3H15M9 21v-3.375c0-.621.504-1.125 1.125-1.125h3.75c.621 0 1.125.504 1.125 1.125V21"
                />
              </svg>
            </span>
            {{ experience.CompanyName }}
            <span class="ml-5 lg:ml-56 flex items-center">
              <span class="inline-flex align-middle mx-2">
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
                    d="M15 10.5a3 3 0 1 1-6 0 3 3 0 0 1 6 0Z"
                  />
                  <path
                    stroke-linecap="round"
                    stroke-linejoin="round"
                    d="M19.5 10.5c0 7.142-7.5 11.25-7.5 11.25S4.5 17.642 4.5 10.5a7.5 7.5 0 1 1 15 0Z"
                  />
                </svg>
              </span>
              {{ experience.Place }}
            </span>
          </h1>

          <h1 class="text-lg flex items-center">
            <span class="inline-flex align-middle mx-2">
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
                  d="M6.75 3v2.25M17.25 3v2.25M3 18.75V7.5a2.25 2.25 0 0 1 2.25-2.25h13.5A2.25 2.25 0 0 1 21 7.5v11.25m-18 0A2.25 2.25 0 0 0 5.25 21h13.5A2.25 2.25 0 0 0 21 18.75m-18 0v-7.5A2.25 2.25 0 0 1 5.25 9h13.5A2.25 2.25 0 0 1 21 11.25v7.5"
                />
              </svg>
            </span>
            {{ experience.Duration }}
          </h1>
        </div>
        <div class="divider"></div>
      </div>
    </div>

    <div class="flex flex-col mt-12">
      <h1 class="text-3xl font-bold mb-6">Education</h1>
      <div v-for="(education, index) in EducationInfo" :key="index">
        <div class="flex justify-between items-center my-5">
          <h1 class="text-2xl">{{ education.Title }}</h1>
          <div class="bg-green-200 px-8 py-2 rounded-full">
            <h3 class="text-green-700 font-bold">{{ education.Status }}</h3>
          </div>
        </div>
        <div class="flex justify-between flex-wrap items-center my-5">
          <h1 class="text-lg flex items-center">
            <span class="inline-flex align-middle mr-2">
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
                  d="M3.75 21h16.5M4.5 3h15M5.25 3v18m13.5-18v18M9 6.75h1.5m-1.5 3h1.5m-1.5 3h1.5m3-6H15m-1.5 3H15m-1.5 3H15M9 21v-3.375c0-.621.504-1.125 1.125-1.125h3.75c.621 0 1.125.504 1.125 1.125V21"
                />
              </svg>
            </span>
            {{ education.Location }}
          </h1>

          <h1 class="text-lg flex items-center">
            <span class="inline-flex align-middle mx-2">
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
                  d="M6.75 3v2.25M17.25 3v2.25M3 18.75V7.5a2.25 2.25 0 0 1 2.25-2.25h13.5A2.25 2.25 0 0 1 21 7.5v11.25m-18 0A2.25 2.25 0 0 0 5.25 21h13.5A2.25 2.25 0 0 0 21 18.75m-18 0v-7.5A2.25 2.25 0 0 1 5.25 9h13.5A2.25 2.25 0 0 1 21 11.25v7.5"
                />
              </svg>
            </span>
            {{ education.Duration }}
          </h1>
        </div>
        <div class="divider"></div>
      </div>
    </div>
  </div>
</template>
