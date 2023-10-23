<template>
  <div
    class="w-full h-full max-w-2xl mx-auto ring rounded-md shadow-sm bg-white min-h-[40vh] p-6 flex flex-col items-start justify-start gap-3"
  >
    <h3 class="text-2xl font-medium text-slate-700/60">Mock form</h3>
    <form
      @submit.prevent="submit"
      class="grow w-full flex flex-col items-start justify-start gap-3"
    >
      <div class="form-control w-full max-w-lg mx-auto">
        <label class="label">
          <span class="label-text">What is your name?</span>
        </label>
        <input
          v-model="form.fullname"
          name="fullname"
          required
          type="text"
          placeholder="Type here"
          class="input input-bordered w-full"
        />
      </div>

      <div class="form-control w-full max-w-lg mx-auto">
        <label class="label">
          <span class="label-text">What is your best email?</span>
        </label>
        <input
          v-model="form.email"
          name="email"
          required
          type="email"
          placeholder="Type here"
          class="input input-bordered w-full"
        />
      </div>

      <button
        type="submit"
        class="mt-8 btn btn-ghost bg-primary text-white hover:bg-primary/80 w-full max-w-lg mx-auto"
      >
        Stay up to date
      </button>
    </form>
  </div>
</template>

<script>
export default {
  data() {
    return {
      form: {
        fullname: "",
        email: "",
      },
    };
  },
  methods: {
    submit() {
      this.$emit("submit", this.form);

      // log the form data
      const { fullname, email } = this.form;
      console.log({ fullname, email });

      // reset the form
      this.form = {
        fullname: "",
        email: "",
      };
    },
  },
};
</script>
