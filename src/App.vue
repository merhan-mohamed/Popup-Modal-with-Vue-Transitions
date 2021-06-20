<template>
  <div id="app">
    <div id="nav">
      <box />
    </div>
  </div>
</template>
<script type="text/javascript">
import box from "./components/box.vue";
export default {
  components: {
    box,
  },
};
</script>

<style>
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}
body {
  font-family: "montserrat", sans-serif;
}
#app {
  position: relative;
  height: 400px;
  display: flex;
  justify-content: center;
  align-items: center;
  overflow-x: hidden;
}
</style>
