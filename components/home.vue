<template>
  <main class="h-full w-full flex flex-col">
    <div class="min-h-[12rem]"></div>

    <div class="relative max-w-7xl w-full mx-auto h-96 px-8 z-10">
      <button
        class="text-lg py-3 px-6 flex items-center justify-start gap-3 bg-primary/10 rounded-md"
      >
        <div class="w-2 h-2 bg-primary rounded-full animate-pulse"></div>
        <span> Mainnet Live </span>
      </button>
      <h1 class="text-9xl max-w-4xl">
        Capture the value
        <span class="text-primary"> you create </span>
      </h1>
    </div>
    <div class="absolute right-0 lg:-mr-[380px] xl:-mr-[100px] z-0">
      <canvas
        id="token-animation-3"
        class="h-[300px] absolute top-0 right-0 mt-[80px] mr-[420px]"
        width="500"
        height="500"
      ></canvas>
      <div
        class="absolute left-0 inset-y-0 w-[478px] bg-[linear-gradient(90deg,#F2EFED_39%,rgba(242,239,237,0)_100%)]"
      ></div>
      <img
        class="mx-auto max-w-[1206px]"
        src="https://archway.io/_nuxt/illustration-50.b39a23b0.png"
        alt=""
      />
    </div>
    <div class="w-full h-96"></div>
    <div class="w-full h-96"></div>
    <div class="w-full h-96"></div>
  </main>
</template>
<!-- 
<script>
import VueThreeSixty from "vue-360";

import "vue-360/dist/css/style.css";

export default {
  name: "360viewer",
  mounted() {
    Vue.use(VueThreeSixty);
  },
};
</script> -->
