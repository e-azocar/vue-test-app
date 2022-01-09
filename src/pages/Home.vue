<template>
  <Layout>
    <div class="wrapper">
      <h1 class="title">My Vue App</h1>

      <form>
        <FormInput @input="name = $event" placeholder="Name" />
        <FormInput type="email" @input="email = $event" placeholder="Email" />
        <FormButton @submit="submitHandler" text="Submit" />
      </form>
      <Snackbar
        v-if="notify.show"
        :message="notify.message"
        :type="notify.type"
        @closed="notify.show = false"
      />
    </div>
  </Layout>
</template>

<script>
import FormInput from "../components/Input.vue";
import FormButton from "../components/Button.vue";
import Snackbar from "../components/Snackbar.vue";
import Layout from "../components/Layout.vue";

export default {
  name: "Home",
  data: () => ({
    name: "",
    email: "",
    notify: {
      show: false,
      message: "",
      type: "",
    },
  }),
  components: {
    FormInput,
    FormButton,
    Snackbar,
    Layout,
  },
  methods: {
    submitHandler() {
      if (!this.name || !this.email) {
        return (this.notify = {
          show: true,
          message: "All fields are required",
          type: "error",
        });
      }

      sessionStorage.setItem(
        "user",
        JSON.stringify({ name: this.name, email: this.email })
      );

      this.$router.push("/result");
    },
  },
};
</script>