<template>
  <div class="fixed inset-x-0 top-4 w-full z-20">
    <div
      class="navbar rounded-md w-full mx-auto transition-all duration-300"
      :class="{
        'bg-white backdrop-blur-sm backdrop-brightness-50 b max-w-6xl':
          scrolled,
        'bg-none max-w-7xl': !scrolled,
      }"
    >
      <div class="navbar-start">
        <div class="dropdown">
          <label tabindex="0" class="btn btn-ghost lg:hidden">
            <svg
              xmlns="http://www.w3.org/2000/svg"
              class="h-5 w-5"
              fill="none"
              viewBox="0 0 24 24"
              stroke="currentColor"
            >
              <path
                stroke-linecap="round"
                stroke-linejoin="round"
                stroke-width="2"
                d="M4 6h16M4 12h8m-8 6h16"
              />
            </svg>
          </label>
          <ul
            tabindex="0"
            class="menu menu-sm dropdown-content mt-3 z-[1] p-2 shadow bg-base-100 rounded-box w-52"
          >
            <li>
              <a>
                <b> Parent </b>
              </a>
              <ul class="p-2">
                <li><a>Submenu 1</a></li>
                <li><a>Submenu 2</a></li>
              </ul>
            </li>
            <li><a>Item 3</a></li>
          </ul>
        </div>
        <a class="btn btn-ghost normal-case text-xl">
          <svg
            viewBox="0 0 120 120"
            fill="none"
            xmlns="http://www.w3.org/2000/svg"
            class="h-6"
          >
            <path
              d="M0 60.48C0 27.0778 26.8629 0 60 0C93.137 0 120 27.0778 120 60.48V119.94C119.968 86.8305 93.1171 60 60 60C26.863 60 5.85937e-05 86.8629 5.85937e-05 120L0 60.48Z"
              fill="currentColor"
            ></path>
          </svg>
          <svg
            width="90"
            height="25"
            viewBox="0 0 90 25"
            fill="none"
            xmlns="http://www.w3.org/2000/svg"
            class="h-6 w-24 transition-all duration-300"
            :class="{ 'w-0': scrolled }"
          >
            <path
              d="M16.8295 20.0571L11.3455 4.04785H6.19501L0.710938 20.0571H3.54681L5.069 15.465H12.4715L13.9937 20.0571H16.8295ZM8.78066 4.38489L11.6999 13.1478H5.84053L8.78066 4.38489Z"
              fill="currentColor"
            ></path>
            <path
              d="M20.2991 8.70317H17.7135V20.0571H20.32V13.6955C20.32 11.7154 21.3 11.0414 23.3226 11.0414H24.0316V8.45039C21.863 8.45039 20.737 9.75641 20.2991 11.4627V8.70317Z"
              fill="currentColor"
            ></path>
            <path
              d="M30.0539 20.3099C32.7438 20.3099 34.8916 18.8353 35.4546 16.139H32.8272C32.4102 17.6136 31.5344 18.4562 30.0539 18.4562C28.1772 18.4562 27.0721 16.8974 27.0721 14.3696C27.0721 11.884 28.1564 10.3041 30.0539 10.3041C31.5553 10.3041 32.4102 11.3573 32.7021 12.6634H35.3503C34.8707 10.1356 32.9315 8.45039 30.0539 8.45039C26.6759 8.45039 24.4239 10.8307 24.4239 14.3696C24.4239 17.9085 26.655 20.3099 30.0539 20.3099Z"
              fill="currentColor"
            ></path>
            <path
              d="M43.0584 8.45039C41.1192 8.45039 40.014 9.63002 39.4927 11.0203V4.04785H36.9071V20.0571H39.5136V13.4638C39.5136 11.2941 40.431 10.3252 41.8907 10.3252C43.3712 10.3252 44.2678 11.2731 44.2678 13.4217V13.4638V20.0571H46.8743V12.9583V12.9161C46.8743 10.3884 45.644 8.45039 43.0584 8.45039Z"
              fill="currentColor"
            ></path>
            <path
              d="M61.2462 19.7832L59.3695 8.70317H54.7404L52.8637 19.7832L50.5283 8.70317H48.0886L50.5074 20.0571H55.22L57.055 8.95595L58.8899 20.0571H63.6025L66.0213 8.70317H63.5816L61.2462 19.7832Z"
              fill="currentColor"
            ></path>
            <path
              d="M71.9728 8.45039C69.2203 8.45039 67.3019 9.86173 67.0309 12.0946H69.6582C69.8042 11.1467 70.5757 10.3041 71.9728 10.3041C73.5367 10.3041 74.2873 11.3784 74.2873 12.7055V12.7476V12.8951L71.3055 13.211C69.1786 13.4217 66.6555 13.9904 66.6555 16.6235C66.6555 18.7721 68.3654 20.3099 70.4923 20.3099C72.64 20.3099 73.5992 19.2988 74.3082 17.8032V20.0571H76.8938V12.8529V12.8108C76.8938 10.4937 75.4342 8.45039 71.9728 8.45039ZM71.4932 18.6458C70.3046 18.6458 69.3037 17.9085 69.3037 16.6235C69.3037 15.149 70.8468 14.9383 72.2647 14.7698L74.2873 14.5592V15.2333C74.2873 17.1291 73.349 18.6458 71.4932 18.6458Z"
              fill="currentColor"
            ></path>
            <path
              d="M83.5836 18.4562L80.1639 8.70317H77.5365L81.1439 18.8353H83.4585L81.8112 24.1858H84.5011L89.3179 8.70317H86.5863L83.5836 18.4562Z"
              fill="currentColor"
            ></path>
          </svg>
        </a>
      </div>
      <div class="navbar-center hidden lg:flex">
        <ul class="menu menu-horizontal px-1">
          <li tabindex="0">
            <div
              class="dropdown hover:text-primary active:bg-primary/10 focus:bg-primary/10 hover:bg-primary/10 visited:bg-primary/20 relative"
            >
              <label
                tabindex="0"
                class="cursor-pointer font-medium flex items-center justify-center gap-2 text-lg"
                >Learn
                <svg
                  xmlns="http://www.w3.org/2000/svg"
                  width="16"
                  height="16"
                  viewBox="0 0 24 24"
                  fill="none"
                  stroke="currentColor"
                  stroke-width="2"
                  stroke-linecap="round"
                  stroke-linejoin="round"
                  class="lucide lucide-chevron-down"
                >
                  <path d="m6 9 6 6 6-6" />
                </svg>
              </label>
              <ul
                tabindex="0"
                class="top-[100%] text-slate-700 mt-2 dropdown-content z-[1] menu p-2 shadow bg-base-100 rounded-box w-52"
              >
                <li><a>Item 1</a></li>
                <li><a>Item 2</a></li>
              </ul>
            </div>
          </li>

          <li tabindex="0">
            <div
              class="dropdown hover:text-primary active:bg-primary/10 focus:bg-primary/10 hover:bg-primary/10 visited:bg-primary/20 relative"
            >
              <label
                tabindex="0"
                class="cursor-pointer font-medium flex items-center justify-center gap-2 text-lg"
                >Developers
                <svg
                  xmlns="http://www.w3.org/2000/svg"
                  width="16"
                  height="16"
                  viewBox="0 0 24 24"
                  fill="none"
                  stroke="currentColor"
                  stroke-width="2"
                  stroke-linecap="round"
                  stroke-linejoin="round"
                  class="lucide lucide-chevron-down"
                >
                  <path d="m6 9 6 6 6-6" />
                </svg>
              </label>
              <ul
                tabindex="0"
                class="top-[100%] text-slate-700 mt-2 dropdown-content z-[1] menu p-2 shadow bg-base-100 rounded-box w-52"
              >
                <li><a>Item 1</a></li>
                <li><a>Item 2</a></li>
              </ul>
            </div>
          </li>

          <li tabindex="0">
            <div
              class="dropdown hover:text-primary active:bg-primary/10 focus:bg-primary/10 hover:bg-primary/10 visited:bg-primary/20 relative"
            >
              <label
                tabindex="0"
                class="cursor-pointer font-medium flex items-center justify-center gap-2 text-lg"
                >Network
                <svg
                  xmlns="http://www.w3.org/2000/svg"
                  width="16"
                  height="16"
                  viewBox="0 0 24 24"
                  fill="none"
                  stroke="currentColor"
                  stroke-width="2"
                  stroke-linecap="round"
                  stroke-linejoin="round"
                  class="lucide lucide-chevron-down"
                >
                  <path d="m6 9 6 6 6-6" />
                </svg>
              </label>
              <ul
                tabindex="0"
                class="top-[100%] text-slate-700 mt-2 dropdown-content z-[1] menu p-2 shadow bg-base-100 rounded-box w-52"
              >
                <li><a>Item 1</a></li>
                <li><a>Item 2</a></li>
              </ul>
            </div>
          </li>

          <li tabindex="0">
            <div
              class="dropdown hover:text-primary active:bg-primary/10 focus:bg-primary/10 hover:bg-primary/10 visited:bg-primary/20 relative"
            >
              <label
                tabindex="0"
                class="cursor-pointer font-medium flex items-center justify-center gap-2 text-lg"
                >Community
                <svg
                  xmlns="http://www.w3.org/2000/svg"
                  width="16"
                  height="16"
                  viewBox="0 0 24 24"
                  fill="none"
                  stroke="currentColor"
                  stroke-width="2"
                  stroke-linecap="round"
                  stroke-linejoin="round"
                  class="lucide lucide-chevron-down"
                >
                  <path d="m6 9 6 6 6-6" />
                </svg>
              </label>
              <ul
                tabindex="0"
                class="top-[100%] text-slate-700 mt-2 dropdown-content z-[1] menu p-2 shadow bg-base-100 rounded-box w-52"
              >
                <li><a>Item 1</a></li>
                <li><a>Item 2</a></li>
              </ul>
            </div>
          </li>
          <li
            class="cursor-pointer font-medium flex items-center justify-center gap-2 text-lg"
          >
            <a
              href="#"
              class="hover:text-primary active:bg-primary/10 focus:bg-primary/10 hover:bg-primary/10 visited:bg-primary/20"
              >Ecosystem</a
            >
          </li>
        </ul>
      </div>
      <div class="navbar-end">
        <a class="btn btn-neutral capitalize">Get in touch</a>
      </div>
    </div>
  </div>
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
