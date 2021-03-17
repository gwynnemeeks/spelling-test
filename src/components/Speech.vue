<template>
  <button @click="sayWord" class="clickable">
    <h3><i class="far fa-play-circle fa-4x"></i></h3>
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

<style>
.fa-play-circle {
  margin-bottom: 20px;
}
</style>
