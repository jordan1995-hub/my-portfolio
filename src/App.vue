<script setup>

import HeroPage from './components/HeroPage.vue';
import ContactUs from './components/ContactUs.vue'
import Skills from './components/Skills.vue';
import MyProjects from './components/MyProjects.vue';
import Footer from './components/Footer.vue';
</script>

<template>
 <div class="px-28 py-5 bg-gray-900 ">
  <header class="sticky top-0 z-10 text-gray-600 body-font">
    <div class="  container mx-auto flex flex-wrap p-5 flex-col md:flex-row items-center">
      <a class="flex title-font font-medium items-center text-gray-900 mb-4 md:mb-0">
        
        <span class="ml-3 text-xl text-indigo-500">< /Dan></span>
      </a>
      <nav class="md:ml-auto flex flex-wrap items-center text-base justify-center">
        <a href="#" @click="scrollTo('hero-page')"  class="mr-5 text-indigo-500 hover:text-indigo-500">Home</a>
        <a  href="#" @click="scrollTo('skills-page')" class="mr-5 cursor-pointer text-white hover:text-indigo-500">Skills</a>
        <a href="#" @click="scrollTo('projects-page')"  class="mr-5 text-white hover:text-indigo-500">Projects</a>
      </nav>

    </div>
  </header>
  <HeroPage id="hero-page" />
  <Skills id="skills-page"/>
  <MyProjects id="projects-page" />
  <ContactUs />
  <Footer  />


 </div>

</template>
<script >
import { ref } from 'vue';

const scrollTo = (sectionId) => {
  const section = document.getElementById(sectionId);
  section.scrollIntoView({ behavior: 'smooth' });
};
</script>
<!-- 
<style scoped>
.logo {
  height: 6em;
  padding: 1.5em;
  will-change: filter;
  transition: filter 300ms;
}
.logo:hover {
  filter: drop-shadow(0 0 2em #646cffaa);
}
.logo.vue:hover {
  filter: drop-shadow(0 0 2em #42b883aa);
}
</style> -->
