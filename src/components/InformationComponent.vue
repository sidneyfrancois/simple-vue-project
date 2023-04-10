<script lang="ts">
export default {
  data() {
    return {
      count: 1,
      obj: {
        nested: { count: 0 },
        arr: ["foo", "bar"],
      },
    };
  },
  methods: {
    increment() {
      this.count++;
    },
    addNewItem() {
      this.obj.arr.push("test");
    },
  },
  mounted() {
    console.log(this.count);
  },
};
</script>

<template>
  <button @click="increment">Click to Add</button>
  Cout is {{ count }}

  <button @click="addNewItem">Add new element</button>
  <h2>{{ obj.arr[obj.arr.length - 1] }}</h2>
  <h3>{{ obj.arr }}</h3>
</template>
