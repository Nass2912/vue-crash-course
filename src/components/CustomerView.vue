<template>
  <div class="container" style="margin-bottom: 2rem">
    <div class="row">
      <div class="col">
        <p class="h3">Customer</p>
        <ul class="list-group">
          <li class="list-group-item">Name : {{ name }}</li>
          <li class="list-group-item">Age : {{ age }}</li>
          <li class="list-group-item">
            Work : {{ work }} and also {{ profession }}
          </li>
        </ul>
      </div>
    </div>
  </div>
  <div class="container">
    <div class="row">
      <div class="col-md-4">
        <div class="card shadow-lg">
          <div class="card-body">
            <p class="h3 display-3">{{ count }}</p>
            <button class="btn btn-success m-1" @click="incr">Increment</button>
            <button class="btn btn-danger m-1" @click="decr">Decrement</button>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "CustomerView",
  props: {
    name: { type: String, required: true },
    age: String,
    work: String,
  },

  data() {
    return {
      profession: "marine",
      count: 0,
    };
  },

  methods: {
    incr() {
      this.count++;
    },

    decr() {
      this.count--;
    },
  },
};
</script>

<style>
</style>