<template>
  <h1>Component loaded</h1>
  <h2>This is the number {{ number }}</h2>
  <button @click="increment">Increment with emit</button>
  <br />
  <br />
  <button @click="incrementNr">Increment with callback fn</button>
</template>

<script>
export default {
  props: {
    number: Number,
    incrementNr: Function,
  },
  emits: ["incNum"],
  methods: {
    increment() {
      this.$emit("incNum");
    },
  },
};
</script>

<style></style>
