<template>
  <div v-if="github">
    <img v-bind:src="github.avatar_url" alt="Profil photo" />
    <p>{{ github.name }}</p>
  </div>
</template>

<script>
// import axios from "axios";
export default {
  created() {},
  name: "Request",
  data() {
    return {
      github: {},
    };
  },
  mounted() {
    fetch("https://api.github.com/users/Alexis-Pannetier")
      .then((response) => response.json())
      .then((data) => (this.github = data));
    // axios
    //   .get("https://api.github.com/users/Alexis-Pannetier")
    //   .then((response) => (this.github = response.data));
  },
};
</script>

<style scoped></style>
