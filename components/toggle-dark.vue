<script setup lang="ts">
import { Button } from './ui/button';

const colorMode = useColorMode();

const isDark = computed({
  get() {
    return colorMode.state.value === 'dark';
  },
  set() {
    colorMode.value = colorMode.value === 'dark' ? 'light' : 'dark';
  },
});
</script>

<template>
  <Button
    variant="ghost"
    size="icon"
    @click="isDark = !isDark"
  >
    <Icon
      :name="isDark ? 'lucide:moon' : 'lucide:sun'"
      size="24"
    />
  </Button>
</template>

<style scoped></style>
