<template>
  <comp :number="number" @incNum="incrementNumber" />
</template>

<script>
import Comp from "./components/Comp.vue";

export default {
  name: "App",
  components: { Comp },
  data() {
    return {
      number: 3,
    };
  },
  methods: {
    incrementNumber() {
      this.number += 2;
    },
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
