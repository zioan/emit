<template>
  <h1>Component loaded</h1>
  <h2>This is the number {{ number }}</h2>
  <button @click="increment">Click to increment with 2</button>
</template>

<script>
export default {
  props: ["number"],
  emits: ["incNum"],
  methods: {
    increment() {
      this.$emit("incNum");
    },
  },
};
</script>

<style></style>
