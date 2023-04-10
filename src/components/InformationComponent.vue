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
    removeItem() {
      this.obj.arr.pop();
    },
    clearData() {
      this.obj.arr = [];
    },
  },
  computed: {
    // computed properties are cached based on their reactive dependencies
    // computed properties are getter-only, must provide manually a getter and setter
    // must be free of side effects
    hasElements() {
      return this.obj.arr.length > 0 ? "Yes" : "No";
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
  <button @click="removeItem">Remove element</button>
  <h2>{{ obj.arr[obj.arr.length - 1] }}</h2>
  <h3>{{ obj.arr }}</h3>

  <br />

  <h2>Has elements: {{ hasElements }}</h2>
</template>
