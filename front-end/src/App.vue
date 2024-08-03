<script setup lang="ts">
import { RouterLink, RouterView } from 'vue-router';

import HelloWorld from './components/HelloWorld.vue';
</script>

<template>
  <header class="borderGuide flex gap-3">
    <img src="@/assets/vue.svg" alt="Vue logo" class="logo vue" />
    <div class="rightSide flex flex-col justify-between">
      <HelloWorld msg="Great!" />
      <nav class="">
        <RouterLink to="/">Home</RouterLink>
        <RouterLink to="/about">About</RouterLink>
      </nav>
    </div>
  </header>

  <div id="rightSide" class="borderGuide">
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
