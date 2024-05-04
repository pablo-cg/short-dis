<script setup lang="ts">
useHead({
  bodyAttrs: {
    class:
      'font-sans antialiased bg-white dark:bg-neutral-900 text-black dark:text-white text selection:bg-neutral-200 dark:selection:bg-neutral-700',
  },
});
</script>

<template>
  <TheHeader />
  <slot />
  <TheFooter />
</template>

<style scoped></style>
