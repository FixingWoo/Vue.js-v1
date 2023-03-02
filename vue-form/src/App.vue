<template>
  <div>
    <form v-on:submit.prevent="formSubmit">
      <div>
        <label for="userName">ID: </label>
        <input id="userName" type="text" v-model="username" />
      </div>
      <div>
        <label for="password">Password:</label>
        <input id="password" type="password" v-model="password" />
      </div>
      <button type="submit">login</button>
    </form>
  </div>
</template>
<script>
import axios from "axios";

export default {
  data: function () {
    return {
      username: "",
      password: "",
    };
  },
  methods: {
    formSubmit: function () {
      // event.preventDefault();
      console.log(this.username, this.password);

      const url = "https://jsonplaceholder.typicode.com/users/";
      const data = {
        username: this.username,
        password: this.password,
      };
      axios
        .post(url, data)
        .then((response) => {
          console.log(response);
        })
        .catch((error) => {
          console.log(error);
        });
    },
  },
};
</script>
<style></style>
