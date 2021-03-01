<template>
  <div class="hello">
    <h2>Vous êtes majeur !</h2>
    <button v-on:click="myMethod">myMethod</button>
  </div>
</template>

<script>
export default {
  name: "Old",
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
