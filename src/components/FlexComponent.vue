<script lang="ts">
export default {
  data() {
    return {};
  },
  methods: {},
};
</script>
<template>
  <div class="flex-container">
    <div class="flex-item">Flex Item 1</div>
    <div class="flex-item">Flex Item 2</div>
    <div class="flex-item">Flex Item 3</div>
  </div>
</template>
<style>
.flex-container {
  width: 70%;
  max-width: 60rem;
  border: 5px solid #000;
  padding: 2em;
}

.flex-item {
  margin: 0 5rem;
  border: 5px solid #aaa;
  background-color: #000;
  color: #fff;
  padding: 0.5em;
}
</style>
