<template>
  <h2>Listing</h2>
  <ul v-for="use in user" :key="use.id">
    <li>Name: {{ use.name }}</li>
    <li>Street: {{ use.address.street }}</li>
  </ul>
</template>

<script>
export default {
  name: "UserView",

  data() {
    return {
      user: [],
    };
  },

  async created() {
    this.user = await this.dataFetch();
    console.log(this.user);
  },

  methods: {
    async dataFetch() {
      const res = await fetch("https://jsonplaceholder.typicode.com/users");

      const data = await res.json();
      return data;
    },
  },
};
</script>

<style>
</style>