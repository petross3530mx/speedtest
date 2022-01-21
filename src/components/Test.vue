<template>
  <div class="grid">
    <div v-for="number of numbers" :key="number" @click="clickNumber(number)">
      {{ number }}
    </div>
  </div>
</template>
<script lang="ts">
import { Component, Vue } from "vue-property-decorator";
@Component
export default class Test extends Vue {
  numbers: number[] = [];
  currentNumber = 0;

  mounted(): void {
    const numbers = [];
    for (let i = 0; i < 25; i++) {
      numbers[i] = i + 1;
    }
    numbers.sort(() => Math.random() - 0.5);
    this.numbers = numbers;
  }

  // eslint-disable-next-line @typescript-eslint/explicit-module-boundary-types
  clickNumber(number: number) {
    if (number - 1 == this.currentNumber) {
      this.currentNumber = number;
      if (number === 25) {
        alert("finish");
      }
    } else {
      this.currentNumber = 0;
      alert("end");
    }
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
  cursor: pointer;
  border: 1px solid #fff;
  align-items: center;
  justify-content: center;
}
</style>
