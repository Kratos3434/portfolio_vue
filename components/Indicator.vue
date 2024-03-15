<template>
  <div class="tw-flex tw-flex-col tw-h-full tw-justify-center tw-items-center tw-absolute tw-right-[16px] tw-gap-5">
    <NuxtLink v-for="link in links" :href="link.path" class="tw-w-[10px] tw-h-[10px] tw-rounded-[50%] hover:tw-bg-[#FBFF48] tw-transition-all" :style="{ backgroundColor: link.color}">
    </NuxtLink>
  </div>
</template>

<script lang="ts">
export default {
    data() {
      return {
        links: [
          {
            name: "Home",
            path: "#home",
            color: this.pos == 0 ? "#FBFF48" : "#CBCBCB"
          },
          {
            name: "About",
            path: "#about",
            color: this.pos == 1 ? "#FBFF48" : "#CBCBCB"
          },
          {
            name: "Work",
            path: "#work",
            color: this.pos == 2 ? "#FBFF48" : "#CBCBCB"
          },
          {
            name: "Projects",
            path: "#projects",
            color: this.pos == 3 ? "#FBFF48" : "#CBCBCB"
          },
          {
            name: "Contact",
            path: "#contact",
            color: this.pos == 4 ? "#FBFF48" : "#CBCBCB"
          }
        ]
      }
    },
    props: ['pos']
  }
</script>