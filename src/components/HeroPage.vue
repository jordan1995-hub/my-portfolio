<template>
    <section class="text-gray-600 body-font">
        <div class="container mx-auto flex px-5 py-24 md:flex-row flex-col items-center">
          <div class="lg:flex-grow md:w-1/2 lg:pr-24 md:pr-16 flex flex-col md:items-start md:text-left mb-16 md:mb-0 items-center text-center">
            <h1 class=" sm:text-4xl text-3xl mb-4 font-medium text-white">I'm a <span></span><span class="text-animation text-indigo-500">{{ typeValue }}</span>
              <span class="cursor" :class="{'typing': typeStatus}">&nbsp;</span>
            </h1>
            <p class="mb-8 leading-relaxed text-white"> {{ aboutMe }}</p>
            <div class="flex justify-center">
              <button class="inline-flex text-white bg-indigo-500 border-0 py-2 px-6 focus:outline-none hover:bg-indigo-600 rounded text-lg">Contact Me</button>
            
            </div>
          </div>
          <div class="lg:max-w-lg lg:w-full md:w-1/2 w-5/6">
            <img class="object-cover object-center rounded" alt="hero" src="/src/assets/Jordan.jpg">
          </div>
        </div>
      </section>
</template>

<script setup>
import { ref, onMounted } from 'vue';


const aboutMe = ref('I am Jordan Canete, an aspiring junior web developer fueled by a passion for coding and a drive to make a meaningful impact through technology. With a thirst for learning and a keen eye for design, I am dedicated to honing my skills and crafting exceptional web experiences.')
const typeValue = ref('');
const typeStatus = ref(true);
const typeArray = ref(['Jordan Canete', 'Web developer', 'Frontend Developer']);
const typingSpeed = ref(200);
const erasingSpeed = ref(100);
const newTextDelay = ref(200);
let typeArrayIndex = ref(0);
let charIndex = ref(0);

const typeText = () => {
  if (charIndex.value < typeArray.value[typeArrayIndex.value].length) {
    if (!typeStatus.value) typeStatus.value = true;

    typeValue.value += typeArray.value[typeArrayIndex.value].charAt(charIndex.value);
    charIndex.value += 1;

    setTimeout(typeText, typingSpeed.value);
  } else {
    typeStatus.value = false;
    setTimeout(eraseText, newTextDelay.value);
  }
};

const eraseText = () => {
  if (charIndex.value > 0) {
    if (!typeStatus.value) typeStatus.value = true;

    typeValue.value = typeArray.value[typeArrayIndex.value].substring(0, charIndex.value - 1);
    charIndex.value -= 1;
    setTimeout(eraseText, erasingSpeed.value);
  } else {
    typeStatus.value = false;
    typeArrayIndex.value += 1;
    if (typeArrayIndex.value >= typeArray.value.length) typeArrayIndex.value = 0;

    setTimeout(typeText, typingSpeed.value + 1000);
  }
};

onMounted(() => {
  setTimeout(typeText, newTextDelay.value + 200);
});
</script>


<style>


span.cursor{
  display: inline-block;
  background-color: #fff;
}
span.cursor.typing{
  animation: none
}
@keyframes cursorBlink {
  49% { background-color: #fff; }
  50% { background-color: transparent; }
  99% { background-color: transparent; }
}
</style>