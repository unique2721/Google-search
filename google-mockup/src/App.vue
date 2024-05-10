<script setup>
import {ref,provide} from 'vue';
const isSearch = ref(false);
provide('isSearch', isSearch)


/* images */
import vue from './assets/images/vue.png'
import dots from './assets/images/dots.jpg'

/* components */
import NavBar from './components/NavBar.vue';
import Links from './components/Links.vue';
import MainLinks from './components/MainLinks.vue'
</script>

<template>
  <NavBar/>
  <div v-if="!isSearch" class="notSearch flex justify-center items-center flex-col mt-[30px]">
    <h1 class="text-[3rem] text-fuchsia-700">Google Mock up</h1>
    <p class="text-[1.2rem] mb-[20px] italic">This is a google search mockup designed by applying the following vue js concepts</p>
    <ul class="outline-2 rounded-2xl w-[400px] text-center mb-[40px]">
      <li class="rounded-t-2xl">Conditional Rendering</li>
      <li>Text Interpolation</li>
      <li>Two way bindnig {v-model}</li>
      <li>reactive states {ref}</li>
      <li>vue components</li>
      <li>Define Props</li>
      <li>Provide and Inject</li>
      <li>Event Handling in vue</li>
      <li class="rounded-b-2xl">Dynamic Binding</li>
    </ul>
  </div>
  <div v-if="isSearch">
  <hr>
  <Links/>
  <div class="flex overflow-hidden inner-container">
    <div>
      <MainLinks link="Vue.js - The Progressive JavaScript Framework | Vue.js" text="The Progressive JavaScript Framework · Approachable. Builds on top of standard HTML, CSS and JavaScript with intuitive API and world-class documentation." href="https://vuejs.org/"/>
      <MainLinks href="https://vuejs.org/guide/introduction" link="Introduction" text="Ways of Using Vue - Quick Start - Tutorial - Composition API FAQ"/>
      <MainLinks href="https://vuejs.org/guide/quick-start" link="Quick Start" text="Creating a Vue Application ​ · $ cd <your-project-name> $ npm ..."/>
      <MainLinks href="https://vuejs.org/tutorial/" link="Tutorial" text="Reactivity Fundamentals - Template Syntax - Watchers"/>
      <MainLinks href="https://vuejs.org/examples/" link="Examples" text="Vue.js - The Progressive JavaScript Framework."/>
      <MainLinks href="https://v2.vuejs.org/" link="Vue 2" text="Introduction - API - Vue 2 EOL - ..."/>
      <MainLinks href="https://www.google.com/search?q=vue+js+site:vuejs.org&sca_esv=33fda89bc4ea5a26&sca_upv=1&rlz=1C1CHBF_enET1103ET1103&sa=X&ved=2ahUKEwjR3OLxooGGAxXQ_7sIHePJAB0QrAN6BAgKEAE" link="More results from vuejs.org »"/>
    </div>
    <div class="outline-2 rounded-[10px] max-w-[350px] ml-[260px]">
      <div class="flex">
        <img :src="vue" alt="vue">
        <img :src="vue" alt="vue">
        <img :src="vue" alt="vue">
      </div>
      <div class="flex">
        <h1 class="text-[1.75rem]">Vue.js</h1>
        <img :src="dots" alt="dots" class="dots w-[20px] h-[20px]">
        <hr>
      </div>
      <p>Vue.js is an open-source model–view–viewmodel front end JavaScript library for building user interfaces and single-page applications. It was created by Evan You, and is maintained by him and the rest of the active core team members. <a href="https://en.wikipedia.org/wiki/Vue.js">Wikipedia</a></p>
      <div>
        <p>Intial rekease date: <span>February 2014</span></p>
        <p>License: <span><a href="https://www.google.com/search?sa=X&sca_esv=33fda89bc4ea5a26&sca_upv=1&rlz=1C1CHBF_enET1103ET1103&biw=1366&bih=641&q=MIT+License&stick=H4sIAAAAAAAAAONgVuLQz9U3MCkryF3Eyu3rGaLgk5mcmlecCgA_x3mRGgAAAA&ved=2ahUKEwinqdPsyYKGAxVUhf0HHUC4AhcQmxMoAXoECE8QAw">MIT License</a></span></p>
        <p>Repository: <span>github.com/vuejs/core</span></p>
        <p>Size: <span><a href="https://www.google.com/search?sa=X&sca_esv=33fda89bc4ea5a26&sca_upv=1&rlz=1C1CHBF_enET1103ET1103&biw=1366&bih=641&q=33.9+KB+min%2Bgzip&stick=H4sIAAAAAAAAAONgVuLQz9U3ME6qKlnEKmBsrGep4O2kkJuZp51elVkAAKXT3h0fAAAA&ved=2ahUKEwinqdPsyYKGAxVUhf0HHUC4AhcQmxMoAXoECFUQAw">33.9 KB min+gzip</a></span></p>
        <p>Written in: <span><a href="https://www.google.com/search?sa=X&sca_esv=33fda89bc4ea5a26&sca_upv=1&rlz=1C1CHBF_enET1103ET1103&biw=1366&bih=641&q=TypeScript&stick=H4sIAAAAAAAAAONgVuLSz9U3yDM1yKgoW8TKFVJZkBqcXJRZUAIA8z90HhsAAAA&ved=2ahUKEwinqdPsyYKGAxVUhf0HHUC4AhcQmxMoAXoECE0QAw">TypeScript</a></span></p>
      </div>
    </div>
  </div>
</div>
</template>

<style scoped>
.notSearch ul li {
  font-size: 1.75rem;
  width: 100%;
}
.notSearch ul li:nth-of-type(even) {
  background-color: orange;
}
.notSearch ul li:nth-of-type(odd) {
  background-color: rgba(0, 0, 255, 0.74);
  color: white;
}
.notSearch ul li:hover {
  background-color: #6114E0;
  cursor: pointer;
  color: white;
}
hr {
  transform: translateY(35px);
}
 img {
  width: 120px;
  height: 120px;
}
span,a {
  color: #6114E0;
}
/* media query*/
@media screen and (max-width: 1100) {
  .container .inner-container {
    margin-left: 200px;
  } 
}
</style>