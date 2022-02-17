<template>
  <div id="app">
    <Test v-if="started" />
    <div v-else>
      <p>
        Test is created to define a level of cognitive ability to work efficient
      </p>
      <p>You will need to find  numbers from 1 to 25 random positioned grid</p>
      <p class="groupped centered">Results can be the next:
        <ul>
          <li>You are tired, lets sleep for 20 minutes to get working state </li>
          <li>Maybe you need to relax before work, think about it</li>
          <li>Go ahead, it's your the most efficient time, Don't spend that time for this test</li>
        </ul>
      </p>
      <button @click="started = true">start</button>
    </div>
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
export default class App extends Vue {
  started = false;
}
</script>

<style>
.groupped.centered{
  max-width: 450px;
  text-align: left;
  display: block;
  margin: auto;
}
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
