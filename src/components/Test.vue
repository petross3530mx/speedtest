<template>
  <div class="grid">
    <div v-for="number of numbers" :key="number">{{ number }}</div>
  </div>
</template>
<script lang="ts">
import { Component, Vue } from "vue-property-decorator";
@Component
export default class Test extends Vue {
  numbers: number[] = [];

  mounted(): void {
    const numbers = [];
    for (let i = 0; i < 25; i++) {
      numbers[i] = i + 1;
    }
    this.numbers = numbers.sort(() => Math.random() - 0.5);
  }
}
</script>
<style scoped>
.grid {
  display: grid;
  grid-template-columns: repeat(5, 3rem);
  grid-template-rows: repeat(5, 3rem);
  margin: auto;
  max-width: 15rem;
}
.grid div {
 display: flex;
  border: 1px solid #fff;
  align-items: center;
  justify-content: center;
}
</style>
