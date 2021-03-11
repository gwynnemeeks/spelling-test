<template>
  <div id="speech">
    <h3>Say Word</h3>
  </div>
</template>

<script>
export default {
  props: ["word"],
  methods: {
    sayWord() {
      const utterance = new SpeechSynthesisUtterance(this.word);
      speechSynthesis.speak(utterance);
    },
  },
};
</script>

<style></style>
