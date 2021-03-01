<template>
  <div class="hello">
    <table class="center">
      <thead>
        <tr>
          <th colspan="2">Liste de course</th>
        </tr>
      </thead>
      <tbody>
        <tr v-for="(item, index) in list" :key="index">
          <td>
            <button @click="removeItem(index)">{{ item }}</button>
          </td>
        </tr>
      </tbody>
    </table>

    <select v-model="itemSelected">
      <option v-for="(item, index) in items" :key="index">
        {{ item }}
      </option>
    </select>

    <button @click="addItem()">Ajouter</button>
  </div>
</template>

<script>
export default {
  created() {},
  name: "List",
  data() {
    return {
      itemSelected: "",
      list: [],
      items: ["orange", "fraise", "framboise", "banane", "cerise"],
      value: 10,
    };
  },
  methods: {
    increment: function() {
      this.value++;
    },
    decrement: function() {
      this.value--;
    },
    addItem: function() {
      this.list.push(this.itemSelected);
    },
    removeItem: function(index) {
      this.list.splice(index, 1);
    },
  },
};
</script>

<style scoped>
table,
td {
  border: 1px solid #333;
}
</style>
