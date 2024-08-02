<script setup lang="ts">
import HelloWorld from './components/HelloWorld.vue';
</script>

<template>
  <!-- <div>
    <a href="https://vitejs.dev" target="_blank">
      <img src="/vite.svg" class="logo" alt="Vite logo" />
    </a>
    <a href="https://vuejs.org/" target="_blank">
      <img src="./assets/vue.svg" class="logo vue" alt="Vue logo" />
    </a>
  </div>
  <HelloWorld msg="Vite + Vue" /> -->
  <div class="flex justify-center items-center">
    <HelloWorld msg="Vite + Vue" />
    <div id="rightSide" class="borderGuide p-2 w-1/2">
      this is the right side
    </div>
  </div>
</template>

<style scoped>
.borderGuide {
  border: 1px solid red;
}
</style>
