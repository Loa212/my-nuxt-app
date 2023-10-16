<template>
  <main class="w-full bg-gray-100 fixed">
    navbar

    <div v-if="scrolled">this is scrolled</div>
  </main>
</template>

<script>
export default {
  name: "navbar",
  data: () => ({
    scrolled: false,
  }),
  methods: {
    handleScroll() {
      this.scrolled = window.scrollY > 56;
    },
  },
  beforeMount() {
    window.addEventListener("scroll", this.handleScroll);
  },
  afterMount() {
    handleScroll();
  },
  beforeDestroy() {
    window.removeEventListener("scroll", this.handleScroll);
  },
};
</script>
