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

    <GreetView />

    <RegisterView />

    <AuthenticateView />
  </div>
</template>

<script>
import CustomerView from "./components/CustomerView.vue";

import GreetView from "./components/GreetView.vue";

import RegisterView from "./components/RegisterView.vue";

import AuthenticateView from "./components/AuthenticateView.vue";

export default {
  components: { CustomerView, GreetView, RegisterView, AuthenticateView },
};
</script>

<style>
</style>
