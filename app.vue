<!-- eslint-disable no-undef -->
<script setup lang="ts">
const sections = {
  japanese: [
    { href: "https://www.wanikani.com/", text: "wanikani" },
    {
      href: "https://www.youtube.com/watch?v=pSvH9vH60Ig&list=PLg9uYxuZf8x_A-vcqqyOFZu06WlhnypWj",
      text: "cure dolly",
    },
    { href: "https://bunpro.jp/", text: "bunpro" },
    {
      href: "https://community.wanikani.com/t/master-list-of-book-clubs/35283",
      text: "books",
    },
    { href: "https://learnjapanese.moe/", text: "resources" },
  ],
  dev: [
    { href: "https://love2d.org/", text: "love2d" },
    { href: "https://wakatime.com/dashboard", text: "wakatime" },
    {
      href: "https://viewsourcecode.org/snaptoken/kilo/index.html",
      text: "diy text editor",
    },
  ],
  keyboard: [
    { href: "https://monkeytype.com/", text: "monkeytype" },
    { href: "https://kbd.news/vendors/Europe", text: "stores" },
    { href: "https://milktooth.com/", text: "switches" },
  ],
  misc: [
    {
      href: "https://www.mariogba.nl/gameboy-advance-spel-info.php?t=Game_Boy_Advance_SP_AGS-101",
      text: "gba sp ags-101",
    },
    { href: "https://fmhy.net/readingpiracyguide", text: "fmhy" },
    { href: "https://cobalt.tools", text: "cobalt" },
  ],
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
        <SearchBar />
        <div
          class="mx-auto grid grid-cols-1 gap-y-12 px-12 md:max-w-screen-sm md:grid-cols-2 md:px-24 lg:max-w-screen-lg lg:grid-cols-4 lg:gap-12"
        >
          <LinkSection
            v-for="(links, title) in sections"
            :key="title"
            :title="title"
            :links="links"
          />
        </div>
      </div>
    </div>
  </div>
</template>
