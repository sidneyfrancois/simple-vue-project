<script lang="ts">
export default {
  data() {
    return {
      count: 1,
    };
  },
  methods: {
    increment() {
      this.count++;
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
</template>
