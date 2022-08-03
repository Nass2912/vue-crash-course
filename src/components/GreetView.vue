<template>
  <h2>Greetings {{ msg }}</h2>
  <button class="btn btn-success m-1" @click="greet('Good')">Good</button>
  <button class="btn btn-success m-1" @click="greet('Bad')">Bad</button>
  <button class="btn btn-success m-1" @click="greet('Worse')">Worse</button>
</template>

<script>
export default {
  name: "GreetView",

  data() {
    return {
      msg: "",
    };
  },

  methods: {
    greet(value) {
      this.msg = value;
    },
  },
};
</script>

<style>
</style>