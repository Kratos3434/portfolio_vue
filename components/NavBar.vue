<template>
  <nav class="tw-flex tw-py-[16px] tw-px-[32px] tw-bg-[hsla(0,0%,100%,.25)] tw-fixed tw-top-0 tw-w-full tw-text-[12.8px] tw-items-center tw-z-[1000]">
    <NuxtLink to="/">
      <img src="/img/kc.jpg" width="90" height="44.41" alt="KC Logo" class="tw-w-[90px] tw-h-[44.41px] tw-rounded-lg" />
    </NuxtLink>
    <div class="tw-flex tw-flex-1 tw-justify-center tw-gap-5">
      <NuxtLink class="tw-text-[12.8px] tw-text-[#6B7688] tw-font-semibold tw-uppercase hover:tw-text-black tw-transition-all" v-for="link in links" :to="link.path">
        {{ link.name }}
      </NuxtLink>
    </div>
  </nav>
</template>

<script lang="ts">
  export default {
    data() {
      return {
        links: [
          {
            name: "Home",
            path: "#home"
          },
          {
            name: "About",
            path: "#about"
          },
          {
            name: "Work",
            path: "#work"
          },
          {
            name: "Projects",
            path: "#projects"
          },
          {
            name: "Contact",
            path: "#contact"
          }
        ]
      }
    }
  }
</script>

<style>
  html {
    scroll-behavior: smooth;
  }
</style>