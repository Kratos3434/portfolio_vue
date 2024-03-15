<template>
  <div class="tw-flex tw-flex-col tw-gap-3 tw-max-w-[190px] tw-w-full hover:tw-scale-[1.1] tw-transition tw-ease-in tw-duration-300">
    <img :src="img" width="190" height="170" alt="software developer" class="tw-rounded-[50px] tw-w-[190px] tw-h-[170px]" />
    <span class="tw-text-[16px] tw-font-bold">{{ title }}</span>
    <span class="tw-text-[12.8px] tw-font-bold tw-text-[#808595]">
      {{ description }}
    </span>
  </div>
</template>

<script>
  export default {
    props: ['img', 'title', 'description' ]
  }
</script>