<script setup lang="ts">
import { UNavigationMenu } from '#components';
import type { NavigationMenuItem } from '@nuxt/ui';

const snsLinks = ref<NavigationMenuItem[][]>([
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

// TODO: リンクをダミーデータにしているのでそれを書き換える
const links = ref<NavigationMenuItem[][]>([
  [
    {
      icon: 'material-symbols:chevron-right-rounded',
      label: 'ホーム',
      to: 'https://www.google.com/'
    },
    {
      icon: 'material-symbols:chevron-right-rounded',
      label: '記事一覧',
      to: 'https://www.google.com/'
    },
    {
      icon: 'material-symbols:chevron-right-rounded',
      label: 'お問い合わせ',
      to: 'https://www.google.com/'
    }
  ]
]);
</script>

<template>
  <div class="bg-surface-500 flex flex-col justify-center">
    <UNavigationMenu
      orientation="horizontal"
      :items="snsLinks"
      class="w-full flex justify-center"
      :ui="{
        link: 'hover:before:bg-transparent flex items-center justify-center w-full px-[2rem]',
        linkLeadingIcon: 'text-black group-hover:opacity-75 w-[26.42px] h-[27px]'
      }"
    />

    <UNavigationMenu
      orientation="vertical"
      :items="links"
      class="w-full flex items-start md:items-center pb-[1.5rem]"
      :ui="{
        link: 'hover:before:bg-transparent text-black font-medium',
        linkLeadingIcon: 'text-black'
      }"
    />
  </div>
</template>
