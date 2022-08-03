<template>
  <div class="container">
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
</template>

<script>
export default {
  name: "CustomerView",
  props: {
    name: { type: String, required: true },
    age: Number,
    work: String,
  },

  data() {
    return {
      profession: "marine",
    };
  },
};
</script>

<style>
</style>