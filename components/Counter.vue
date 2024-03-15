
<template>
  <h1 class="tw-text-[60px] tw-text-center tw-font-semibold">Counter App</h1>
  <div class="tw-flex tw-justify-center tw-m-10">
    <div class="tw-flex tw-gap-4 tw-items-center">
      <button v-on:click="decreaseCounter()" class="tw-rounded-md tw-bg-gray-200 tw-p-2">
        -
      </button>
      {{ count }}
      <button v-on:click="increaseCounter()">
        +
      </button>
    </div>
  </div>
</template>

<script lang="ts">
  export default {
    data() {
      return {
        count: 0,
      }
    },
    methods: {
      increaseCounter() {
        this.count++;
      },
      decreaseCounter() {
        this.count--;
      }
    }
  }
</script>