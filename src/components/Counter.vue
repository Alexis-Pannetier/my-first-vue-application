<template>
  <div class="hello">
    <h2>Compteur</h2>
    <p>{{ value }}</p>
    <button v-on:click="decrement()">-</button>
    <button v-on:click="increment()">+</button>
  </div>
</template>

<script>
export default {
  name: "Counter",
  data() {
    return { value: 10 };
  },
  methods: {
    increment: function() {
      this.value++;
    },
    decrement: function() {
      this.value--;
    },
  },
};
</script>

<style scoped></style>
