<template>
  <section class="tw-h-[100dvh] tw-w-full tw-bg-[#EFF2F8] tw-px-[16px] tw-pt-[76.41px]" id="work">
    <div class="tw-w-full tw-h-full tw-flex tw-flex-col tw-justify-center tw-items-center">
      <span class="tw-text-[44px] tw-font-bold">Skills & Experience</span>
      <div class="tw-flex tw-gap-10 tw-mt-[48px] tw-justify-center tw-w-full">
        <div class="tw-flex tw-flex-wrap tw-gap-5 tw-justify-center tw-max-w-[447px] tw-w-full">
          <div v-for="logo in logos" class="tw-flex tw-flex-col tw-items-center tw-gap-3">
            <div class="tw-flex tw-justify-center tw-bg-white tw-rounded-[50%] tw-w-[90px] tw-h-[90px] tw-items-center">
              <img :src="logo.path" width="45" height="45" :alt="logo.name" class="tw-w-[45px] tw-h-[45px]" />
            </div>
            <span class="tw-text-[12.8px]">
              {{ logo.name }}
            </span>
          </div>
        </div>
        <div class="tw-flex tw-flex-col tw-text-[16px]">
          <div class="tw-flex tw-gap-5">
            <span class="tw-text-[#6D5FBD]">July 2023 - Present</span>
            <div class="tw-text-center tw-flex tw-flex-col tw-items-start">
              <span class="tw-text-semibold">Full Stack Developer</span>
              <span>Dmsolving</span>
            </div>
          </div>
        </div>
      </div>
      <Indicator pos="2" />
    </div>
  </section>
</template>

<script setup lang="ts">
const logos = useState('logos', () => [
  {
    path: '/img/c++.png',
    name: 'C++',
  },
  {
    path: '/img/react.png',
    name: 'React',
  },
  {
    path: '/img/python.png',
    name: 'Python',
  },
  {
    path: '/img/next.svg',
    name: 'Next Js',
  },
  {
    path: '/img/svelte.png',
    name: 'Svelte Kit',
  },
  {
    path: '/img/sql.svg',
    name: 'SQL',
  },
  {
    path: '/img/mongo.svg',
    name: 'Mongo DB',
  },
  {
    path: '/img/aws.png',
    name: 'AWS',
  },
  {
    path: '/img/tailwind.png',
    name: 'Tailwind CSS',
  },
  {
    path: '/img/node.png',
    name: 'Node Js',
  },
  {
    path: '/img/git.png',
    name: 'Git',
  },
  {
    path: '/img/js.png',
    name: 'JavaScript',
  },
]);


</script>