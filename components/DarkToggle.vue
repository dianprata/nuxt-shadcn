<script setup lang="ts">
const color = useColorMode()

useHead({
  meta: [{
    id: 'theme-color',
    name: 'theme-color',
    content: () => color.value === 'dark' ? '#000000' : '#ffffff',
  }],
})

function toggleDark() {
  color.preference = color.value === 'dark' ? 'light' : 'dark'
}
</script>

<template>
  <button class="!outline-none" title="Toggle Color Scheme" aria-label="button dark toggle" @click="toggleDark">
    <div class="i-carbon-sun dark:i-carbon-moon !h-5 !w-5" />
  </button>
</template>
