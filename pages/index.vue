<script setup lang="ts">
import { Button } from '~/components/ui/button';
useHead({
  titleTemplate() {
    return 'ShortDis - A blatant copy of an open-source URL Shortner';
  },
});
</script>

<template>
  <main class="relative h-[calc(100vh-4rem)]">
    <div
      id="background"
      class="absolute inset-0 -z-10 h-full w-full bg-white bg-[linear-gradient(to_right,#8080800a_1px,transparent_1px),linear-gradient(to_bottom,#8080800a_1px,transparent_1px)] bg-[size:24px_24px] dark:bg-neutral-900"
    />

    <div
      id="hero"
      class="px-6 pt-16 md:pt-24 lg:pt-32"
    >
      <section class="mt-10 text-center space-y-5">
        <h1
          class="font-bold text-5xl tracking-tight duration-500 animate-in fade-in-5 slide-in-from-bottom-2"
        >
          Enhance your Link Management
        </h1>
        <p
          class="text-pretty text-sm md:text-base duration-700 animate-in fade-in-5 slide-in-from-top-2"
        >
          ShortDis is an open-source app where you can create, manage and share
          short links. It is easy to use, fast and secure.
        </p>
      </section>
      <section class="flex gap-2 justify-center mt-8">
        <Button
          as-child
          variant="secondary"
          class="h-12 px-5"
        >
          <NuxtLink to="/dashboard">
            <Icon
              name="lucide:link"
              size="18"
              class="mr-2"
            />
            Create a Link
          </NuxtLink>
        </Button>
        <Button
          as-child
          variant="outline"
          class="h-12 px-5"
        >
          <NuxtLink
            to="https://github.com/pablo-cg/short-dis"
            target="_blank"
          >
            <Icon
              name="lucide:github"
              size="18"
              class="mr-2"
            />
            Star on GitHub
          </NuxtLink>
        </Button>
      </section>
    </div>
  </main>
</template>

<style scoped></style>
