<template>
  <div class="hello">
    <h2>Vous êtes mineur</h2>
    <button v-on:click="myMethod">myMethod</button>
  </div>
</template>

<script>
export default {
  watch: {},
  name: "Young",
  data() {
    return { age: 25 };
  },
  methods: {
    myMethod: function() {
      alert("Coucou 🙃");
    },
  },
};
</script>

<style scoped></style>
