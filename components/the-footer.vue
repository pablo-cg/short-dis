<script setup lang="ts"></script>

<template>
  <footer
    class="w-full text-sm animate-in fade-in-25 text-neutral-600 dark:text-neutral-400 bg-white/60 backdrop-blur-md dark:bg-neutral-900/60 fixed bottom-0 mt-4 py-4"
  >
    <div class="container flex items-center justify-between">
      <div class="flex items-center">
        <section>
          <Icon
            name="lucide:heart"
            class="text-red-600 mr-1"
          />

          <NuxtLink
            to="https://nuxt.com"
            target="_blank"
          >
            Made by Pablo using
            <Icon
              name="tabler:brand-nuxt"
              size="20"
            />
            <Icon name="lucide:arrow-up-right" />
          </NuxtLink>
          <p class="text-xs">
            A blatant copy of
            <NuxtLink
              to="https://slug.vercel.app/"
              target="_blank"
            >
              slug
            </NuxtLink>
            by
            <NuxtLink
              to="https://github.com/pheralb"
              target="_blank"
            >
              @pheralb
            </NuxtLink>
          </p>
        </section>
      </div>
    </div>
  </footer>
</template>

<style scoped></style>
