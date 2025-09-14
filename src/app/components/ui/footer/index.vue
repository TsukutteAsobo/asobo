<script setup lang="ts">
import type { NavigationMenuItem } from '@nuxt/ui';

const items = ref<NavigationMenuItem[][]>([
  [
    {
      icon: 'simple-icons:x',
      to: 'https://x.com/tokumemo0000'
    },
    {
      icon: 'simple-icons:instagram',
      to: 'https://www.instagram.com/tokumemo0000/'
    },
    {
      icon: 'simple-icons:discord',
      to: 'https://discord.com/invite/Tn5U5qKg9A'
    },
    {
      icon: 'simple-icons:github',
      to: 'https://github.com/tokudai0000'
    }
  ]
]);
</script>

<template>
  <UNavigationMenu
    orientation="horizontal"
    :items="items"
    class="w-full flex justify-center"
    :ui="{
      link: 'hover:before:bg-transparent flex items-center justify-between w-full mr-[100%] ml-[100%] ',
      linkLeadingIcon: 'text-black group-hover:opacity-75 w-[36.42px] h-[27px]'
    }"
  />
</template>
