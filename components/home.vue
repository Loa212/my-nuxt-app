<template>
  <main
    class="relative h-full w-full flex flex-col overflow-x-clip selection:bg-primary selection:text-white"
  >
    <div class="min-h-[12rem]"></div>

    <div class="relative max-w-7xl w-full mx-auto h-96 px-8 z-10">
      <button
        class="text-lg py-3 px-6 flex items-center justify-start gap-3 bg-primary/10 rounded-md"
      >
        <div class="w-2 h-2 bg-primary rounded-full animate-pulse"></div>
        <span> Mainnet Live </span>
      </button>
      <h1 class="text-9xl max-w-4xl mb-4">
        Capture the value
        <span class="text-primary"> you create </span>
      </h1>
      <div class="font-medium">
        <p>An incentivized L1 blockchain that allows</p>
        <p>developers to capture the value their dapps</p>
        <p>create, enabling sustainable economic models.</p>
      </div>
    </div>
    <div class="absolute right-0 lg:-mr-[380px] xl:-mr-[100px] z-0">
      <ArchCoin />
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
