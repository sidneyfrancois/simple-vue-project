<script setup lang="ts">
import { ref, reactive } from 'vue';

const reactiveVariable = ref(25);

function addVarible() {
    reactiveVariable.value++;
}
</script>

<template>
    <h2>{{ reactiveVariable }}</h2>
    <button type="button" @click="addVarible">Click to add</button>
</template>