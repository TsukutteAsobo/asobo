<script setup lang="ts">
const authors = ref({
  Hika: {
    name: 'Hika',
    description: 'hika138',
    avatar: {
      src: 'https://github.com/hika138.png'
    },
    to: 'https://github.com/hika138',
    target: '_blank'
  },
  rinngo: {
    name: 'rinngo',
    description: 'rinngo0302',
    avatar: {
      src: 'https://github.com/rinngo0302.png'
    },
    to: 'https://github.com/rinngo0302',
    target: '_blank'
  },
  AZM: {
    name: 'AZM0624',
    description: 'AZM0624',
    avatar: {
      src: 'https://github.com/AZM0624.png'
    },
    to: 'https://github.com/AZM0624',
    target: '_blank'
  }
});

const articles = ref([
  {
    title: 'Test Article',
    description: 'これはテスト用の記事です。',
    image: 'https://nuxt.com/assets/blog/nuxt-icon/cover.png',
    date: '2025-11-4',
    to: 'https://go.nuxt.com/articles/000000',
    authors: [authors.value['Hika']],
    badges: [
      { label: 'Test' },
      { label: 'Test' }
    ]
  },
  {
    title: 'Test Article',
    description: 'これはテスト用の記事です。',
    image: 'https://nuxt.com/assets/blog/nuxt-icon/cover.png',
    date: '2025-11-4',
    to: 'https://go.nuxt.com/articles/000000',
    authors: [authors.value['AZM']],
    badges: [
      { label: 'Test' },
      { label: 'Test' }
    ]
  },
  {
    title: 'Test Article',
    description: 'これはテスト用の記事です。',
    image: 'https://nuxt.com/assets/blog/nuxt-icon/cover.png',
    date: '2025-11-4',
    to: 'https://go.nuxt.com/articles/000000',
    authors: [authors.value['rinngo']],
    badges: [
      { label: 'Test' },
      { label: 'Test' }
    ]
  }
]);
</script>

<template>
  <UContainer>
    <UCard>
      <UBlogPosts>
        <UBlogPost
          v-for="(post, index) in articles"
          :key="index"
          v-bind="post"
        >
          <template #badge>
            <div v-if="post.badges && post.badges.length > 0" class="flex gap-2">
              <UBadge
                v-for="badge in post.badges"
                :key="badge.label"
                v-bind="badge"
              />
            </div>
          </template>
        </UBlogPost>
      </UBlogPosts>
    </UCard>
  </UContainer>
</template>
