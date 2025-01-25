<script setup lang="ts">
interface Link {
  href: string;
  text: string;
}

defineProps<{
  title: string;
  links: Link[];
}>();
</script>

<template>
  <div class="flex flex-col">
    <h2 class="mb-5 text-2xl text-perfume">{{ title }}</h2>
    <a
      v-for="link in links"
      :key="link.href"
      :href="link.href"
      class="mb-4 text-2xl decoration-froly hover:underline"
    >
      {{ link.text }}
    </a>
  </div>
</template>