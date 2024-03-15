<template>
  <section class="about-md:tw-h-[100dvh] tw-w-full tw-bg-[#FFFFFF] tw-px-[16px] tw-pt-[76.41px] tw-pb-10" id="about">
    <div class="tw-h-full tw-w-full tw-flex tw-flex-col tw-justify-center tw-items-center tw-gap-20">
      <h2 class="tw-text-[44px] tw-font-bold tw-text-center" ref="headingRef">
        I Know That <span class="tw-text-[#3D29A7]">Great Code</span> <br />
        Means <span class="tw-text-[#3D29A7]">Great Business</span>
      </h2>
      <div class="tw-flex tw-gap-10 tw-text-start tw-justify-center tw-flex-wrap" ref="skillRef">
        <AboutCard img="/img/sd.jpg" title="Software Developer" description="I am a developer who likes solving complex problems and developing/coding is my passion" />
        <AboutCard img="/img/fs.avif" title="Full Stack Developer" description="My knowledge in full stack development allows me to develop anything with confidence" />
        <AboutCard img="/img/learner.jpg" title="Always Learning" description="I always love learning about new technologies as technology evelove more often" />
        <AboutCard img="/img/team.png" title="Team Player" description="I like working with people and I have experience in an agile environment" />
      </div>
      <Indicator pos="1" />
    </div>
  </section>
</template>

<script setup>
  import { useMotion } from '@vueuse/motion';
  const skillRef = ref();
  const headingRef = ref();

  useMotion(skillRef, {
    initial: { opacity: 0, x: -200 },
    visible: {
      opacity: 1,
      x: 0,
      transition: {
        ease: 'easeIn',
        type: 'keyframes',
        delay: 200
      }
    }
  });

  useMotion(headingRef, {
    initial: { opacity: 0, x: 0 },
    visible: {
      opacity: 1,
      x: 0,
      transition: {
        ease: 'easeIn',
        type: 'keyframes',
        delay: 200
      }
    }
  })
</script>