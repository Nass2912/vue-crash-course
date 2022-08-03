<template>
  <div class="container">
    <div class="grid">
      <div class="row">
        <div class="col">
          <p class="h3 text-success fw-bold">class component</p>
          <p class="fst-italic">
            Lorem ipsum dolor sit amet consectetur adipisicing elit. Possimus
            modi culpa harum, necessitatibus perferendis magnam incidunt
            temporibus. Porro, dolore distinctio.
          </p>
        </div>
      </div>
    </div>

    <CustomerView name="greg" age="25" work="SE" />
  </div>
</template>

<script>
import CustomerView from "./components/CustomerView.vue";

export default {
  components: { CustomerView },
};
</script>

<style>
</style>
