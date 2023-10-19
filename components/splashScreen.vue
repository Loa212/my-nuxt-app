<template>
  <div
    class="absolute inset-0 z-50 flex justify-center items-center w-full h-full bg-primary transition-transform duration-500 ease-in-out transform"
    :class="{ 'translate-y-0': loading, '-translate-y-full': !loading }"
  >
    <div class="h-[18rem] w-[12rem] rounded-full bg-white relative">
      <div
        class="absolute inset-0 flex justify-center items-center w-full h-full transition-transform duration-500 ease-in-out transform"
        :class="{ 'translate-y-0': circle, 'translate-y-[40%]': !circle }"
      >
        <div
          class="h-full w-full rounded-full bg-primary ring ring-primary"
        ></div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "splashScreen",
  data: () => ({
    loading: true,
    circle: true,
  }),
  mounted() {
    // disable scroll
    document.body.style.overflow = "hidden";

    // lower the circle
    setTimeout(() => {
      this.circle = false;
    }, 1500);

    // hide the loader
    setTimeout(() => {
      this.loading = false;
      // enable scroll
      document.body.style.overflow = "auto";
    }, 2500);
  },
};
</script>
