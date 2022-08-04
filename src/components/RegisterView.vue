<template>
  <pre>{{ user }}</pre>
  <div class="container" style="margin-top: 2rem">
    <div class="row">
      <div class="col-md-3">
        <div class="card">
          <div class="card-header bg-warning">
            <p class="h3">Register Here</p>
          </div>
          <div class="card-body">
            <form @submit.prevent="submitForm()">
              <div class="mb-2">
                <input
                  v-model="user.name"
                  type="text"
                  placeholder="name"
                  class="form-control"
                />
              </div>
              <div class="mb-2">
                <input
                  v-model="user.email"
                  type="email"
                  placeholder="email"
                  class="form-control"
                />
              </div>
              <div class="mb-2">
                <input
                  v-model="user.password"
                  type="password"
                  placeholder="password"
                  class="form-control"
                />
              </div>
              <div class="mb-2">
                <input type="submit" class="btn btn-success" />
              </div>
            </form>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "RegisterView",

  data() {
    return {
      user: {
        name: "",
        email: "",
        password: "",
      },
    };
  },

  methods: {
    submitForm() {
      console.log(this.user);
    },
  },
};
</script>

<style>
</style>