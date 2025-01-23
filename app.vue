<!-- eslint-disable no-undef -->
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
  <div class="h-screen content-center text-center">
    <NuxtRouteAnnouncer />
    <div class="flex flex-col text-center 2xl:flex-row">
      <div
        class="flex flex-[2] items-center justify-center p-12 2xl:justify-end"
      >
        <img src="/img/cat.gif" alt="" class="w-64 2xl:w-[34rem]" />
      </div>
      <div class="flex-[3]">
        <h1
          class="mb-12 flex items-center justify-center text-5xl text-malibu 2xl:mb-24"
        >
          <Icon name="feather:chevron-right" class="mr-2 text-bright_equator" />
          スタート。
          <!-- 魂スリヴァー -->
        </h1>
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
        <div
          class="mx-auto grid grid-cols-1 gap-y-12 px-12 md:max-w-screen-sm md:grid-cols-2 md:px-24 lg:max-w-screen-lg lg:grid-cols-4 lg:gap-12"
        >
          <div class="flex flex-col">
            <h2 class="mb-5 text-2xl text-perfume">japanese</h2>
            <a
              href="https://www.wanikani.com/"
              class="mb-4 text-2xl decoration-froly hover:underline"
              >wanikani</a
            >
            <a
              href="https://www.youtube.com/watch?v=pSvH9vH60Ig&list=PLg9uYxuZf8x_A-vcqqyOFZu06WlhnypWj"
              class="mb-4 text-2xl decoration-froly hover:underline"
              >cure dolly</a
            >
            <a
              href="https://bunpro.jp/"
              class="mb-4 text-2xl decoration-froly hover:underline"
              >bunpro</a
            >
            <a
              href="https://community.wanikani.com/t/master-list-of-book-clubs/35283"
              class="mb-4 text-2xl decoration-froly hover:underline"
              >books</a
            >
            <a
              href="https://learnjapanese.moe/"
              class="mb-4 text-2xl decoration-froly hover:underline"
              >resources</a
            >
          </div>
          <div class="flex flex-col">
            <h2 class="mb-5 text-2xl text-perfume">dev</h2>
            <a
              href="https://love2d.org/"
              class="mb-4 text-2xl decoration-froly hover:underline"
              >love2d</a
            >
            <a
              href="https://wakatime.com/dashboard"
              class="mb-4 text-2xl decoration-froly hover:underline"
              >wakatime</a
            >
            <a
              href="https://viewsourcecode.org/snaptoken/kilo/index.html"
              class="mb-4 text-2xl decoration-froly hover:underline"
              >diy text editor</a
            >
          </div>
          <div class="flex flex-col">
            <h2 class="mb-5 text-2xl text-perfume">keyboard</h2>
            <a
              href="https://monkeytype.com/"
              class="mb-4 text-2xl decoration-froly hover:underline"
              >monkeytype</a
            >
            <a
              href="https://kbd.news/vendors/Europe"
              class="mb-4 text-2xl decoration-froly hover:underline"
              >stores</a
            >
            <a
              href="https://milktooth.com/"
              class="mb-4 text-2xl decoration-froly hover:underline"
              >switches</a
            >
          </div>
          <div class="flex flex-col">
            <h2 class="mb-5 text-2xl text-perfume">misc</h2>
            <a
              href="https://www.mariogba.nl/gameboy-advance-spel-info.php?t=Game_Boy_Advance_SP_AGS-101"
              class="mb-4 text-2xl decoration-froly hover:underline"
              >gba sp ags-101</a
            >
            <a
              href="https://fmhy.net/readingpiracyguide"
              class="mb-4 text-2xl decoration-froly hover:underline"
              >fmhy</a
            >
            <a
              href="https://cobalt.tools"
              class="mb-4 text-2xl decoration-froly hover:underline"
              >cobalt</a
            >
          </div>
        </div>
      </div>
    </div>
  </div>
</template>
