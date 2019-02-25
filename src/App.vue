<template>
  <div id="app">
    <exchange />
  </div>
</template>

<script>
import Dep from "@/components/Dep";
import Exchange from "@/components/Exchange";

export default {
  name: "App",
  components: {
    Dep,
    Exchange
  }
};
</script>

<style>
#app {
  background-color: cadetblue;
}
body {
  margin: 0px;
}
#app > table {
  width: 100%;
  height: 100%;
}
table {
  border: 1px solid red;
}
</style>
