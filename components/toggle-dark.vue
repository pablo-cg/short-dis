<script setup lang="ts">
import { Button } from '@/components/ui/button';
import {
  DropdownMenu,
  DropdownMenuContent,
  DropdownMenuItem,
  DropdownMenuLabel,
  DropdownMenuSeparator,
  DropdownMenuTrigger,
} from '@/components/ui/dropdown-menu';

const colorMode = useColorMode();
</script>

<template>
  <ClientOnly>
    <DropdownMenu>
      <DropdownMenuTrigger as-child>
        <Button
          variant="ghost"
          size="icon"
        >
          <Icon
            name="radix-icons:moon"
            class="h-[1.2rem] w-[1.2rem] rotate-0 scale-100 transition-all dark:-rotate-90 dark:scale-0"
          />
          <Icon
            name="radix-icons:sun"
            class="absolute h-[1.2rem] w-[1.2rem] rotate-90 scale-0 transition-all dark:rotate-0 dark:scale-100"
          />
          <span class="sr-only">Toggle theme</span>
        </Button>
      </DropdownMenuTrigger>
      <DropdownMenuContent
        align="end"
        class="dark:bg-neutral-900"
      >
        <DropdownMenuLabel class="font-normal">
          <p className="text-sm font-medium leading-none">Theme</p>
        </DropdownMenuLabel>
        <DropdownMenuSeparator />
        <DropdownMenuItem
          @click="colorMode.preference = 'light'"
          class="flex items-center space-x-3"
        >
          <Icon name="radix-icons:sun" />
          <span>Light</span>
        </DropdownMenuItem>
        <DropdownMenuItem
          @click="colorMode.preference = 'dark'"
          class="flex items-center space-x-3"
        >
          <Icon name="radix-icons:moon" />
          <span>Dark</span>
        </DropdownMenuItem>
        <DropdownMenuItem
          @click="colorMode.preference = 'system'"
          class="flex items-center space-x-3"
        >
          <Icon name="radix-icons:desktop" />
          <span>System</span>
        </DropdownMenuItem>
      </DropdownMenuContent>
    </DropdownMenu>
    <template #fallback>
      <Button
        variant="ghost"
        size="icon"
      >
        <Icon
          name="radix-icons:moon"
          class="h-[1.2rem] w-[1.2rem] rotate-0 scale-100 transition-all dark:-rotate-90 dark:scale-0"
        />
        <Icon
          name="radix-icons:sun"
          class="absolute h-[1.2rem] w-[1.2rem] rotate-90 scale-0 transition-all dark:rotate-0 dark:scale-100"
        />
        <span class="sr-only">Toggle theme</span>
      </Button>
    </template>
  </ClientOnly>
</template>
