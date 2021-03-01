<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png" />

    <div v-if="age >= 18">
      <Old class="content" />
    </div>
    <div v-else>
      <Young class="content" />
    </div>
    <Counter class="content" />
    <List class="content" />
    <Request class="content" />
  </div>
</template>

<script>
import Counter from "./components/Counter.vue";
import List from "./components/List.vue";
import Old from "./components/Old.vue";
import Request from "./components/Request.vue";
import Young from "./components/Young.vue";

export default {
  name: "App",
  data() {
    return { age: 18 };
  },
  components: {
    Counter,
    List,
    Old,
    Request,
    Young,
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
.center {
  margin: auto;
}
.content {
  margin-top: 12px;
  margin-bottom: 12px;
}
</style>
