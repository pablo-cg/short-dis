<script setup lang="ts">
import { Button } from './ui/button';
</script>

<template>
  <nav class="flex w-full pb-3 pt-4 lg:px-4 sticky top-0">
    <div class="flex w-full items-center justify-between container">
      <section>
        <NuxtLink
          to="/"
          class="flex items-center space-x-2 transition-opacity hover:opacity-80"
        >
          <Icon
            name="fa6-solid:link"
            size="36"
            class="p-1 text-neutral-700 dark:text-neutral-100 border border-neutral-400 dark:border-neutral-600 rounded-lg shadow-lg"
          />
          <span>ShortDis</span>
        </NuxtLink>
      </section>
      <section class="flex">
        <Button
          as-child
          variant="ghost"
          size="icon"
        >
          <NuxtLink
            to="https://github.com/pablo-cg/short-dis"
            target="_blank"
          >
            <Icon
              name="lucide:github"
              size="24"
              class="text-neutral-700 dark:text-neutral-100"
            />
          </NuxtLink>
        </Button>

        <Command />

        <ToggleDark />

        <UserButton />
      </section>
    </div>
  </nav>
</template>

<style scoped></style>
