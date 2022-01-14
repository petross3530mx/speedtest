<template>
  <div id="app">
    <Test />
  </div>
</template>

<script lang="ts">
import { Component, Vue } from "vue-property-decorator";
import Test from "./components/Test.vue";

@Component({
  components: {
    Test,
  },
})
export default class App extends Vue {}
</script>

<style>
body {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #fff;
  background: #000;
  margin-top: 60px;
}
</style>
