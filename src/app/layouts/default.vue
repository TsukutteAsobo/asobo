<script setup lang="ts">
import type { NavigationMenuItem } from '#ui/types';

const snsLinks = ref<NavigationMenuItem[]>([
  {
    icon: 'i-simple-icons-discord',
    to: 'https://go.nuxt.com/discord'
  },
  {
    icon: 'i-simple-icons-x',
    to: 'https://go.nuxt.com/x'
  },
  {
    icon: 'i-simple-icons-github',
    to: 'https://github.com/nuxt/nuxt'
  },
  {
    icon: 'i-simple-icons-instagram',
    to: 'https://go.nuxt.com/instagram'
  }
]);

const pageLinks = ref<NavigationMenuItem[]>([
  {
    icon: 'i-lucide-chevron-right',
    label: 'ホーム',
    to: 'https://go.nuxt.com/'
  },
  {
    icon: 'i-lucide-chevron-right',
    label: '記事一覧',
    to: 'https://go.nuxt.com/articles'
  },
  {
    icon: 'i-lucide-chevron-right',
    label: 'お問い合わせ',
    to: 'https://go.nuxt.com/contact'
  }
]);
</script>

<template>
  <div>
    <UHeader title="ASOBO" to="https://go.nuxt.com/" :toggle="false">
      <template #right>
        <USlideover side="top" title="ASOBO">
          <UButton
            icon="i-lucide-menu"
            color="neutral"
            variant="ghost"
            aria-label="Menu"
          />

          <template #body>
            <UNavigationMenu
              :items="pageLinks"
              :ui="{ linkLabel: 'font-semibold' }"
              orientation="vertical"
              variant="link"
              color="neutral"
            />
            <UNavigationMenu
              color="neutral"
              class="justify-center"
              :items="snsLinks"
            />
          </template>
        </USlideover>
      </template>
    </UHeader>
    <UContainer>
      <slot />
    </UContainer>
    <UFooter>
      <template #left>
        <div class="text-sm text-neutral-500">
          © 2025 TUCURO
        </div>
      </template>
      <template #right>
        <div>
          <!-- TODO: リンクは変える -->
          <UButton
            icon="i-simple-icons-discord"
            color="neutral"
            variant="ghost"
            to="https://go.nuxt.com/discord"
            target="_blank"
            aria-label="Discord"
          />
          <UButton
            icon="i-simple-icons-x"
            color="neutral"
            variant="ghost"
            to="https://go.nuxt.com/x"
            target="_blank"
            aria-label="X"
          />
          <UButton
            icon="i-simple-icons-github"
            color="neutral"
            variant="ghost"
            to="https://github.com/nuxt/nuxt"
            target="_blank"
            aria-label="GitHub"
          />
          <UButton
            icon="i-simple-icons-instagram"
            color="neutral"
            variant="ghost"
            to="https://go.nuxt.com/instagram"
            target="_blank"
            aria-label="Instagram"
          />
        </div>
      </template>
    </UFooter>
  </div>
</template>
