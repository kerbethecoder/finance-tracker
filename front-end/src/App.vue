<script setup lang="ts">
import { RouterLink, RouterView } from 'vue-router';

import HelloWorld from './components/HelloWorld.vue';
</script>

<template>
  <header class="flex gap-3">
    <img src="@/assets/vue.svg" alt="Vue logo" class="logo vue" />
    <div class="rightSide">
      <HelloWorld msg="Great!" />
      <nav class="mt-3 flex gap-3">
        <RouterLink to="/" class="text-[#EBEBEB99] underline underline-offset-2"
          >Home</RouterLink
        >
        <div class="text-gray-400 font-bold">|</div>
        <RouterLink
          to="/about"
          class="text-[#EBEBEB99] underline underline-offset-2"
          >About</RouterLink
        >
      </nav>
    </div>
  </header>

  <div id="rightSide" class="flex justify-center items-center">
    <RouterView />
  </div>
</template>

<style scoped>
.borderGuide {
  border: 1px solid red;
}

.logo {
  height: 10em;
  padding: 1em;
  will-change: filter;
  transition: filter 300ms;
}

.logo.vue:hover {
  filter: drop-shadow(0 0 2em #42b883aa);
}
</style>
