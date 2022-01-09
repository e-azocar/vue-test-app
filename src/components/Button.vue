<template>
  <button @click="submitHandler">{{ text }}</button>
</template>

<script>
export default {
  name: "Button",
  props: {
    text: {
      type: String,
      required: true,
    },
  },
  methods: {
    submitHandler(e) {
      e.preventDefault();
      this.$emit("submit");
    },
  },
};
</script>

<style scoped>
button {
  width: 100%;
  padding: 1rem;
  border-radius: 5px;
  border: none;
  cursor: pointer;
  margin: 0.25rem 0;
  background: #41b883;
  color: #252525;
}
button:hover {
  background: #3dad7b;
}
button:active {
  background: #4cd698;
}
</style>