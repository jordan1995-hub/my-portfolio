<template>
  <section class="text-gray-600 body-font">
    <div class="container px-5 py-24 mx-auto">
      <div class="flex flex-col text-center w-full mb-20 ">
        <h1 class="sm:text-3xl text-2xl font-medium title-font mb-4 text-white">{{ title }}</h1>
      </div>
      <div class="flex  flex-wrap justify-center m-4 text-center">
        <div v-for="(skill, index) in skills" :key="index" class="p-4 xl:w-1/4 md:w-2/12 min-w-[200px]  w-96 ">
          <div class="border-2 drop-shadow-2xl bg-white border-indigo-700 px-4 py-6 rounded-lg transform hover:bg-indigo-300 transition duration-500 hover:scale-125">
            <img :src="skill.icon" class=" w-12 h-12 mb-3 inline-block" alt="Skill Icon">
            <h2 class="title-font font-medium text-sm lg:text-xl  text-indigo-500">{{ skill.name }}</h2>
          </div>
        </div>
    
      </div>
    </div>
  </section>
</template>

<script setup>
import { ref } from 'vue'

const title = ref('My Skills')
const skills = ref([
  {name:'HTML', icon: "/public/assets/logo5.png"},
  {name:'CSS', icon: "/public/assets/logo6.png"},
  {name:'JAVASCRIPT', icon: "/public/assets/logo4.png"},
  {name:'TAILWIND CSS', icon: "/public/assets/logo7.png"},
  {name:'GIT', icon: "/public/assets/logo3.png"},
  {name:'VUE JS', icon: "/public/assets/logo9.png"},
  {name:'UI/UX DESIGN', icon: "/public/assets/logo2.png"},
  {name:'WORDPRESS ', icon: "/public/assets/logo1.png"},
  
])
</script>