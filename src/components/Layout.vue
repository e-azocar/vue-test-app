<template>
  <div class="container">
    <slot />
  </div>
</template>

<script>
export default {};
</script>

<style>
.container {
  height: 100vh;
  display: flex;
  align-items: center;
  justify-content: center;
  background: #41b883;
}
.wrapper {
  width: 600px;
  height: fit-content;
  padding: 1rem;
  background: #fff;
  border-radius: 5px;
}
.title {
  font-size: 2.2rem;
  text-align: center;
  font-weight: bold;
  color: #252525;
}
</style>