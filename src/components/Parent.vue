<script lang="ts">
export default {
  data() {
    return {};
  },
  methods: {
    changeWidth() {},
  },
};
</script>

<template>
  <div class="parent">
    <div class="child">
      Lorem ipsum dolor sit amet consectetur adipisicing elit. Officiis delectus
      a omnis aperiam repellendus blanditiis repellat eum iste quia ipsam
      corporis expedita possimus cupiditate laborum libero debitis doloribus,
      est quasi architecto tempore totam. Illum, facilis, sint aspernatur
      laborum labore recusandae aperiam pariatur eaque sapiente, nesciunt
      repellat soluta architecto placeat quibusdam totam blanditiis voluptate
      dolore nulla quae! Officia libero sunt numquam corrupti cumque totam nisi
      nobis excepturi laudantium! Quod voluptate veritatis adipisci mollitia
      beatae deleniti sit explicabo quia doloremque, quidem, eum cumque sint
      accusantium reprehenderit possimus? Esse dolorem assumenda fugiat quas,
      maiores inventore veritatis eligendi nulla corrupti eaque maxime impedit
      eveniet!
    </div>
  </div>

  <div class="button-change-style">
    <button @click="changeWidth">Click to change style</button>
  </div>
</template>

<style>
.parent {
  background-color: #23424a;
  padding: 50px;
  margin: 0 auto;
  width: 80%;
}

.child {
  padding: 3em;
  color: black;
  background-color: #38cfd9;
  width: 60%;
}

.button-change-style {
  background-color: grey;
}
</style>
