<template>
  <div id="app">
    <img alt="logo" src="logo.png" width="150" />
    <FormComponent @add-user="addUser" />
    <TableComponent :users="users" />
  </div>
</template>

<script>
import FormComponent from "./components/FormComponent.vue";
import TableComponent from "./components/TableComponent.vue";

export default {
  name: "App",
  data: () => ({
    users: [],
  }),
  components: { FormComponent, TableComponent },
  methods: {
    addUser(user) {
      this.users.push({
        ...user,
      });
    },
  },
};
</script>

<style>
@import url("https://fonts.googleapis.com/css2?family=Hind+Siliguri:wght@300&family=Lora&family=Raleway:wght@100&display=swap");

:root {
  background: rgb(238, 174, 202);
  background: radial-gradient(
    circle,
    rgba(238, 174, 202, 1) 0%,
    rgba(148, 187, 233, 1) 100%
  );
}

#app {
  font-family: "Hind Siliguri", sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: black;
  margin-top: 60px;
  background: rgb(238, 174, 202);
  background: radial-gradient(
    circle,
    rgba(238, 174, 202, 1) 0%,
    rgba(148, 187, 233, 1) 100%
  );
}
</style>
