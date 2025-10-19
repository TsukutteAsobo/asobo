<script setup lang="ts">

</script>

<template>
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
    </template>
  </UFooter>
</template>
