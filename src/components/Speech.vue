<template>
  <button @click="sayWord" class="clickable">
    <h3>Click Here for Test Word</h3>
  </button>
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
