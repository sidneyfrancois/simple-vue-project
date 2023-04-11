<script lang="ts">
export default {
  data() {
    return {
      isPink: true,
    };
  },
  methods: {
    toggleBackgroundPink() {
      this.isPink = !this.isPink;
    },
  },
};
</script>
<template>
  <div class="flex-container">
    <div class="flex-item">
      Lorem ipsum dolor sit amet consectetur adipisicing elit. Quos, aut vel,
      deserunt nulla recusandae, consequatur voluptas blanditiis magni aliquam
      unde laudantium. Sed aperiam quibusdam explicabo, cumque eius sunt! Nihil
      consectetur distinctio explicabo obcaecati necessitatibus placeat, sint
      quas facere sit dicta laborum quaerat neque quia esse labore vitae velit,
      corrupti incidunt.
    </div>
    <div class="flex-item">Flex Item 2</div>
    <div class="flex-item" :class="{ pinkBackground: isPink }">Flex Item 3</div>
  </div>
  <button @click="toggleBackgroundPink">Toggle Background Pink</button>
</template>
<style>
.flex-container {
  width: 70%;
  max-width: 60rem;
  border: 5px solid #000;
  padding: 2em;
  display: flex;
}

.flex-item {
  margin: 0.5rem;
  border: 5px solid #aaa;
  background-color: #000;
  color: #fff;
  padding: 0.5em;
  width: 100%;
}

.pinkBackground {
  background-color: pink;
}
</style>
