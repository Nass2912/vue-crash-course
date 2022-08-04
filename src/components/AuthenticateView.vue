<template>
  <div class="container">
    <div class="row">
      <div class="col-md-6">
        <div class="card">
          <div class="card-body">
            <div v-if="isLogged">
              <p class="h3 text-success">Welcome User</p>
              <p>
                Lorem ipsum dolor sit amet consectetur, adipisicing elit.
                Veritatis obcaecati, cumque nobis voluptate aspernatur odio amet
                placeat cupiditate aut a nesciunt modi dignissimos accusantium
                asperiores quas. Non, numquam? Quasi, fugit!
              </p>
            </div>
            <div v-else>
              <p class="h3 text-danger">Thank You</p>
              <p style="color: blue">
                Lorem ipsum dolor sit amet consectetur, adipisicing elit.
                Veritatis obcaecati, cumque nobis voluptate aspernatur odio amet
                placeat cupiditate aut a nesciunt modi dignissimos accusantium
                asperiores quas. Non, numquam? Quasi, fugit!
              </p>
            </div>
            <div>
              <button
                class="btn btn-success m-2"
                @click="login()"
                v-if="!isLogged"
              >
                login
              </button>
              <button class="btn btn-danger m-2" @click="logout()" v-else>
                Logout
              </button>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "AuthenticateView",

  data() {
    return {
      isLogged: false,
    };
  },

  methods: {
    login() {
      this.isLogged = true;
    },
    logout() {
      this.isLogged = false;
    },
  },
};
</script>

<style>
</style>