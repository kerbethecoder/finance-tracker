<script setup lang="ts">
defineProps<{ msg: string }>();
</script>

<template>
  <div class="p-2 flex items-center w-1/2">
    <div class="">
      <img src="@/assets/vue.svg" alt="Vue logo" class="logo vue" />
    </div>
    <div>
      <h1>{{ msg }}</h1>
      <p class="text-xl text-[#EBEBEB99]">
        You've successfully created a project with
        <a href="https://vitejs.dev/" target="_blank" rel="noopener noreferrer"
          >Vite
        </a>
        +
        <a href="https://vuejs.org/" target="_blank" rel="noopener noreferrer"
          >Vue 3
        </a>
        +
        <a
          href="https://tailwindcss.com/"
          target="_blank"
          rel="noopener noreferrer"
          >Tailwind</a
        >.
      </p>
    </div>
  </div>
</template>

<style scoped>
.logo {
  height: 20em;
  padding: 1em;
  will-change: filter;
  transition: filter 300ms;
}
.logo.vue:hover {
  filter: drop-shadow(0 0 2em #42b883aa);
}
</style>
