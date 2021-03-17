<template>
  <div>
    <p>Results: {{ correctCount }} / {{ data.length }}</p>
    <p v-if="perfectScore">PERFECT SCORE!</p>
    <p v-else-if="goodjob">Good Job! Just a little bit more practice</p>
    <p v-else-if="morework">Looks like you need more practice. You got this!</p>
  </div>
</template>

<script>
export default {
  props: ["data"],
  computed: {
    correctCount() {
      return this.data.filter((q) => {
        return q.word.toLowerCase() === q.userInput.toLowerCase();
      }).length;
    },
    perfectScore() {
      return this.correctCount === this.data.length;
    },
    goodjob() {
      return this.correctCount != this.perfectScore && this.correctCount >= 7;
    },
    morework() {
      return this.correctCount <= 6;
    },
  },
};
</script>

<style></style>
