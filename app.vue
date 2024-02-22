<template>
  <div class="h-screen w-screen dark:bg-[#0b0b0b] flex justify-center items-center">
    <button @click="toggleTheme">
      <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 16 16" class="theme-icon fill-[#FFF]"
        v-if="$colorMode.value == 'dark'">
        <path
          d="M14.438 10.148c.19-.425-.321-.787-.748-.601A5.5 5.5 0 0 1 6.453 2.31c.186-.427-.176-.938-.6-.748a6.501 6.501 0 1 0 8.585 8.586" />
      </svg>

      <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 16 16" class="theme-icon fill-[#000]" v-else>
        <path
          d="M8 1a.75.75 0 0 1 .75.75v1.5a.75.75 0 0 1-1.5 0v-1.5A.75.75 0 0 1 8 1m2.5 7a2.5 2.5 0 1 1-5 0a2.5 2.5 0 0 1 5 0m2.45-3.89a.75.75 0 1 0-1.06-1.06l-1.062 1.06a.75.75 0 0 0 1.061 1.062zM15 8a.75.75 0 0 1-.75.75h-1.5a.75.75 0 0 1 0-1.5h1.5A.75.75 0 0 1 15 8m-3.11 4.95a.75.75 0 0 0 1.06-1.06l-1.06-1.062a.75.75 0 0 0-1.062 1.061zM8 12a.75.75 0 0 1 .75.75v1.5a.75.75 0 0 1-1.5 0v-1.5A.75.75 0 0 1 8 12m-2.828-.11a.75.75 0 0 0-1.061-1.062L3.05 11.89a.75.75 0 1 0 1.06 1.06zM4 8a.75.75 0 0 1-.75.75h-1.5a.75.75 0 0 1 0-1.5h1.5A.75.75 0 0 1 4 8m.11-2.828A.75.75 0 0 0 5.173 4.11L4.11 3.05a.75.75 0 1 0-1.06 1.06z" />
      </svg>
    </button>
  </div>
</template>

<script setup>
const colorMode = useColorMode();
const toggleTheme = () => {
  colorMode.preference = colorMode.preference === 'dark' ? 'light' : 'dark';
};

</script>

<style>
.theme-icon {
  @apply w-10 h-10 cursor-pointer transition-transform duration-100;
}

.theme-icon:hover {
  @apply scale-125;
}
</style>
