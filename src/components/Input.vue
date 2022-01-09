<template>
  <input
    :type="type"
    :placeholder="placeholder"
    :name="name"
    :id="id"
    autocomplete="off"
    @input="$emit('input', $event.target.value)"
  />
</template>

<script>
export default {
  props: {
    value: {
      type: String,
      default: "",
      required: false,
    },
    placeholder: {
      type: String,
      default: "",
    },
    type: {
      type: String,
      default: "text",
    },
    name: {
      type: String,
      default: "",
    },
    id: {
      type: String,
      default: "",
    },
  },
};
</script>

<style scoped>
input {
  width: 100%;
  padding: 1rem;
  border-radius: 5px;
  border: 1px solid #ccc;
  margin: 0.25rem 0;
}

input:active,
input:focus {
  outline: #41b88391 solid 2px;
}
</style>