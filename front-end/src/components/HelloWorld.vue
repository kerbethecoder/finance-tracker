<script setup lang="ts">
defineProps<{ msg: string }>();
</script>

<template>
  <div class="flex items-center">
    <div>
      <h1 class="text-left font-bold">{{ msg }}</h1>
      <p class="text-xl text-[#EBEBEB99] text-left">
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

<style scoped></style>
