<template>
  <div id="app" v-cloak>
    <router-view> Hello </router-view>
  </div>
</template>
<script>
export default {
  name: "app",
};
</script>

<style>
* {
  box-sizing: border-box;
}
body {
  padding: 0;
  margin: 0;
  height: 100vh;
}
#app {
  font-family: "Arial";
  height: 100vh;
}
</style>