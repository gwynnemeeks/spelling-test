<template>
  <div>
      <p>Results: {{ correctCount }} / {{ questions.length }}</p>
</template>

<script>
export default {
    props: ["questions"],
    computed: {
        correctCount() {
            return this.questions.filter(q => {
                return q.word.toLowerCase() === q.userInput.toLowerCase();
            }).length;
        },
    }
};
</script>

<style>

</style>