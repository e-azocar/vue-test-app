<template>
  <Layout>
    <div class="wrapper">
      <h1 class="title">Result</h1>

      <ul class="result-list">
        <li>
          Name: <b>{{ name }}</b>
        </li>
        <li>
          Email: <b>{{ email }}</b>
        </li>
      </ul>

      <Button text="Return to Home" @submit="returnToHome" />
    </div>
  </Layout>
</template>

<script>
import Button from "../components/Button.vue";
import Layout from "../components/Layout.vue";
export default {
  name: "Result",
  data: () => ({
    name: "",
    email: "",
  }),
  components: {
    Layout,
    Button,
  },
  methods: {
    returnToHome() {
      sessionStorage.clear();
      return this.$router.push("/");
    },
  },
  mounted() {
    const user = sessionStorage.getItem("user");
    if (!user) {
      this.$router.push("/");
    } else {
      const { name, email } = JSON.parse(user);
      this.name = name;
      this.email = email;
    }
  },
};
</script>

<style scoped>
.result-list * {
  font-size: 1.2rem;
}
</style>