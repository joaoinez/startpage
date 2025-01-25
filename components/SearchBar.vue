<script setup lang="ts">
const text = ref("");
const selectedEngine = ref<"google" | "4get">("google");

const handleInput = (e: unknown) => {
  text.value = (e as { target: { value: string } }).target.value;
};

const search = () => {
  const engines = {
    google: `https://google.com/search?q=${text.value.replaceAll(" ", "+")}`,
    "4get": `https://4get.ch/web?s=${text.value.replaceAll(" ", "+")}`,
  };

  window.location.href = encodeURI(engines[selectedEngine.value]);
};
</script>

<template>
  <div class="mb-12 flex justify-center 2xl:mb-24">
    <div class="flex w-1/2 items-center rounded-full bg-fiord px-6 py-4">
      <Icon name="feather:search" class="mr-4 block" />
      <input
        autofocus
        placeholder="search"
        class="w-full bg-transparent text-xl outline-none"
        @input="handleInput"
        @keydown.enter="search"
      />
      <select
        v-model="selectedEngine"
        class="text-md ml-4 cursor-pointer bg-transparent outline-none"
      >
        <option value="google">Google</option>
        <option value="4get">4get</option>
      </select>
    </div>
  </div>
</template>

