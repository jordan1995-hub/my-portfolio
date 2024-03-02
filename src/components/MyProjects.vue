<template>
    <section class="text-gray-600 body-font">
        <div class="container px-5 py-24 mx-auto">
          <div class="flex flex-wrap w-full mb-20">
            <div class="lg:w-1/2 w-full mb-6 lg:mb-0">
              <h1 class="sm:text-3xl text-2xl font-medium title-font mb-2 text-white">My Projects</h1>
              <div class="h-1 w-20 bg-indigo-500 rounded"></div>
            </div>
            <p class="lg:w-1/2 w-full leading-relaxed text-gray-400">{{ title }}</p>
          </div>
          <div class="flex flex-wrap -m-4">
            <div class="xl:w-1/4 md:w-1/2 p-4">
              <div class="bg-gray-100 p-6 rounded-lg">
                <img class="object-cover object-center rounded" alt="hero" src="/public/assets/Jordan.jpg">
                <h3 class="tracking-widest text-indigo-500 text-xs font-medium title-font">BIKE E-COMMERCE</h3>
                <h2 class="text-lg text-gray-900 font-medium title-font mb-4">VUE JS/TAILWIND</h2>
                <p class="leading-relaxed text-base">Lorem ipsum is placeholder text commonly used in the graphic, print, and publishing industries for previewing layouts and visual mockups.</p>
              </div>
            </div>
            <div class="xl:w-1/4 md:w-1/2 p-4">
              <div class="bg-gray-100 p-6 rounded-lg">
                <img class="object-cover object-center rounded" alt="hero" src="/public/assets/Jordan.jpg">
                <h3 class="tracking-widest text-indigo-500 text-xs font-medium title-font">VUE JS CRUD</h3>
                <h2 class="text-lg text-gray-900 font-medium title-font mb-4">VUES/TAILWIND</h2>
                <p class="leading-relaxed text-base">Lorem ipsum is placeholder text commonly used in the graphic, print, and publishing industries for previewing layouts and visual mockups.</p>
              </div>
            </div>
            <div class="xl:w-1/4 md:w-1/2 p-4">
              <div class="bg-gray-100 p-6 rounded-lg">
                <img class="object-cover object-center rounded" alt="hero" src="/public/assets/Jordan.jpg">
                <h3 class="tracking-widest text-indigo-500 text-xs font-medium title-font">LEARNING WEBSITE</h3>
                <h2 class="text-lg text-gray-900 font-medium title-font mb-4">VUE JS/ TAILWIND</h2>
                <p class="leading-relaxed text-base">Lorem ipsum is placeholder text commonly used in the graphic, print, and publishing industries for previewing layouts and visual mockups.</p>
              </div>
            </div>
            <div class="xl:w-1/4 md:w-1/2 p-4">
              <div class="bg-gray-100 p-6 rounded-lg">
                <img class="object-cover object-center rounded" alt="hero" src="/public/assets/Jordan.jpg">
                <h3 class="tracking-widest text-indigo-500 text-xs font-medium title-font">SIMPLE PROJECTS</h3>
                <h2 class="text-lg text-gray-900 font-medium title-font mb-4">HTML/CSS/JAVASCRIPT</h2>
                <p class="leading-relaxed text-base text-overflow-ellipsis  line-clamp-3">Lorem ipsum is placeholder text commonly used in the graphic, print, and publishing industries for previewing layouts and visual mockups.</p>
              </div>
            </div>
          </div>
        </div>
      </section>
</template>

<script setup>
import { ref } from 'vue'


const title = ref('Following projects showcases my skills and experience through real-world examples of my work Each project is briefly described with links to code repositories and live demos in it. It reflects my ability to solve complex problems, work with different technologies, and manage projects effectively.')
</script>