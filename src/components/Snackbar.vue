<template>
  <div class="snackbar" :class="type">{{ message }}</div>
</template>

<script>
export default {
  name: "Snackbar",
  props: {
    message: {
      type: String,
      required: true,
    },
    type: {
      type: String,
      required: true,
    },
  },
  methods: {
    start() {
      setTimeout(() => {
        this.$emit("closed");
      }, 2000);
    },
  },
  mounted() {
    this.start();
  },
};
</script>

<style scoped>
.snackbar {
  padding: 1rem;
  border-radius: 5px;
  max-width: 16rem;
  position: fixed;
  top: 1rem;
  right: 1rem;
  animation: fadeIn 1s;
  transition: opacity 0.5s;
}
.snackbar.success {
  background: #d1e7dd;
  color: #0f5132;
}
.snackbar.error {
  background: #e7d1d1;
  color: #9b0d0d;
}
.snackbar.active {
  opacity: 1;
}

@keyframes fadeIn {
  0% {
    opacity: 0;
  }
  100% {
    opacity: 1;
  }
}
</style>