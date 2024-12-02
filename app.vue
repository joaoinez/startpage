<template>
  <div class="h-screen content-center text-center">
    <NuxtRouteAnnouncer />
    <div class="flex flex-wrap content-center justify-center text-center">
      <div class="flex flex-[2] content-center justify-end">
        <img src="/img/cat.gif" alt="" class="w-[34rem]" />
      </div>
      <div class="flex-[3]">
        <h1
          class="mb-12 flex content-center justify-center text-5xl text-malibu"
        >
          <Icon name="feather:chevron-right" class="mr-2 text-bright_equator" />
          スタート。
          <!-- 魂スリヴァー -->
        </h1>
        <div class="mb-12">
          <input type="text" autofocus />
        </div>
        <div class="flex flex-wrap justify-around px-12">
          <div class="flex flex-col px-12">
            <h2 class="mb-5 text-3xl text-perfume">japanese</h2>
            <a href="https://www.wanikani.com/" class="mb-4 text-2xl"
              >wanikani</a
            >
            <a
              href="https://www.youtube.com/watch?v=pSvH9vH60Ig&list=PLg9uYxuZf8x_A-vcqqyOFZu06WlhnypWj"
              class="mb-4 text-2xl"
              >cure dolly</a
            >
            <a href="https://bunpro.jp/" class="mb-4 text-2xl">bunpro</a>
            <a
              href="https://community.wanikani.com/t/master-list-of-book-clubs/35283"
              class="mb-4 text-2xl"
              >books</a
            >
            <a href="https://learnjapanese.moe/" class="mb-4 text-2xl"
              >resources</a
            >
          </div>
          <div class="flex flex-col px-12">
            <h2 class="mb-5 text-3xl text-perfume">dev</h2>
            <a href="https://love2d.org/" class="mb-4 text-2xl">love2d</a>
          </div>
          <div class="flex flex-col px-12">
            <h2 class="mb-5 text-3xl text-perfume">keyboard</h2>
            <a href="https://www.wanikani.com/" class="mb-4 text-2xl"
              >monkeytype</a
            >
            <a href="https://kbd.news/vendors/Europe" class="mb-4 text-2xl"
              >stores</a
            >
            <a href="https://milktooth.com/" class="mb-4 text-2xl">switches</a>
          </div>
          <div class="flex flex-col px-12">
            <h2 class="mb-5 text-3xl text-perfume">misc</h2>
            <a
              href="https://www.mariogba.nl/gameboy-advance-spel-info.php?t=Game_Boy_Advance_SP_AGS-101"
              class="mb-4 text-2xl"
              >gba sp ags-101</a
            >
            <a href="https://fmhy.net/readingpiracyguide" class="mb-4 text-2xl"
              >fmhy</a
            >
          </div>
        </div>
      </div>
    </div>
  </div>
</template>
