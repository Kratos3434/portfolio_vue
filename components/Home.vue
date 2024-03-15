<template>
  <section
    class="home-lg:tw-h-[100dvh] tw-bg[#6B7688] tw-pt-[76.41px] tw-px-[16px] tw-bg-[url('https://lucasmoncada.netlify.app/static/media/bgIMG.c39101e520e2997fc6d4.png')] tw-bg-cover"
    id="home">
    <div class="tw-w-full tw-h-full tw-flex tw-justify-center home-lg:tw-flex-row tw-flex-col">
      <!--Left side-->
      <div class="tw-flex tw-flex-col tw-gap-9 home-lg:tw-items-end tw-items-center">
          <div
            class="tw-px-[32px] tw-py-[16px] tw-flex tw-rounded-xl tw-bg-[#EFF2F8] tw-shadow-lg tw-gap-5 tw-items-center tw-m-2"
            ref="sideRef">
            <span class="tw-text-[40px]">👋</span>
            <div class="tw-flex tw-flex-col">
              <span class="tw-text-[12.8px] tw-text-[#6B7688]">Hello, I am</span>
              <span class="tw-text-black tw-font-bold tw-text-[44px]">Keith</span>
            </div>
          </div>
          <div
            class=" tw-rounded-xl tw-px-[32px] tw-py-[16px] tw-shadow-2xl tw-flex tw-flex-col tw-text-[12.8px] tw-text-[#6B7688] tw-text-end tw-uppercase tw-font-semibold"
            ref="sideRef2">
            <span>Software Developer</span>
            <span>Full Stack Developer</span>
          </div>
        </div>
        <!--Left side end-->
        <!--Image-->
        <div class="tw-flex home-lg:tw-items-end home-lg:tw-justify-normal tw-justify-center">
          <img src="https://lucasmoncada.netlify.app/static/media/Portfolio-Picture.e1a8950a835a89247ec2.png"
            width="600" height="640" alt="profile" class="tw-object-contain tw-overflow-clip home-lg:tw-w-full home-lg:tw-h-full tw-w-[600px] sm:tw-h-[640px] tw-h-[600px]" ref="imgRef" />
        </div>
        <!--Image End-->
      <!--Language logos-->
      <div class="tw-flex home-lg:tw-flex-col tw-items-start tw-justify-center sm:tw-gap-10 tw-gap-5 home-lg:tw-mt-0 tw-mt-10">
        <div class="tw-rounded-[1000px] tw-shadow-xl tw-flex tw-justify-center tw-bg-white tw-p-4" ref="reactRef">
          <img src="https://lucasmoncada.netlify.app/static/media/react.20adfb35ae6a6e5817bf.png" width="54" height="54"
            class="sm:tw-w-[54px] sm:tw-h-[54px] tw-w-[34px] tw-h-[34px] tw-bg-white" />
        </div>
        <div class="tw-rounded-[1000px] tw-shadow-xl tw-flex tw-justify-center tw-bg-white tw-p-6 tw-m-[24px]"
          ref="cppRef">
          <img src="/img/c++.png" width="75" height="75" class="sm:tw-w-[75px] sm:tw-h-[75px] tw-bg-white tw-w-[55px] tw-h-[55px]" />
        </div>
        <div class="tw-rounded-[1000px] tw-shadow-xl tw-flex tw-justify-center tw-bg-white tw-p-4" ref="pyRef">
          <img src="/img/python.png" width="54" height="54" class="sm:tw-w-[54px] sm:tw-h-[54px] tw-w-[34px] tw-h-[34px] tw-bg-white" />
        </div>
      </div>
      <!--Language Logos END-->
      <Indicator pos="0" />
    </div>
  </section>
</template>

<script setup>
import { useMotion } from '@vueuse/motion';
const sideRef = ref();
const sideRef2 = ref();
const reactRef = ref();
const cppRef = ref();
const pyRef = ref();
const imgRef = ref();

useMotion(sideRef, {
  initial: { opacity: 0, x: -200  },
  visible: {
    opacity: 1,
    x: 0,
    transition: {
      ease: 'easeIn',
      type: 'keyframes'
    }
  }
})

useMotion(sideRef2, {
  initial: { opacity: 0, x: -200  },
  visible: {
    opacity: 1,
    x: 0,
    transition: {
      ease: 'easeIn',
      delay: 200,
      type: 'keyframes'
    }
  }
})

useMotion(reactRef, {
  initial: { opacity: 0, x: 100, y: 100 },
  visible: {
    opacity: 1,
    x: 0,
    y: 0,
    transition: {
      ease: 'easeIn',
      delay: 200,
      type: 'keyframes'
    }
  }
});

useMotion(cppRef, {
  initial: { opacity: 0, x: 200 },
  visible: {
    opacity: 1,
    x: 0,
    transition: {
      ease: 'easeIn',
      delay: 200,
      type: 'keyframes'
    }
  }
});

useMotion(pyRef, {
  initial: { opacity: 0, x: 100, y: -50 },
  visible: {
    opacity: 1,
    x: 0,
    y: 0,
    transition: {
      ease: 'easeIn',
      delay: 200,
      type: 'keyframes'
    }
  }
});

useMotion(imgRef, {
  initial: { opacity: 0, y: -200 },
  visible: {
    opacity: 1,
    y: 0,
    transition: {
      ease: 'easeIn',
      type: 'keyframes',
    }
  }
})
</script>