<template>
  <UContainer>
    <slot />
  </UContainer>
  <UFooter>
      <template #right>
      <UButton
        icon="i-simple-icons-discord"
        color="neutral"
        variant="ghost"
        to="https://discord.com/invite/Tn5U5qKg9A"
        target="_blank"
        aria-label="Discord"
      />
      <UButton
        icon="i-simple-icons-x"
        color="neutral"
        variant="ghost"
        to="https://x.com/tokumemo0000"
        target="_blank"
        aria-label="X"
      />
      <UButton
        icon="i-simple-icons-github"
        color="neutral"
        variant="ghost"
        to="https://github.com/TsukutteAsobo/asobo"
        target="_blank"
        aria-label="GitHub"
      />
      <UButton
        icon="i-simple-icons-instagram"
        color="neutral"
        variant="ghost"
        to="https://www.instagram.com/tokumemo0000/"
        target="_blank"
        aria-label="Instagram"
      />
    </template>
    <div class="text-center">
      © 2024 TUCURO. All rights reserved.
    </div>
  </UFooter>
</template>
