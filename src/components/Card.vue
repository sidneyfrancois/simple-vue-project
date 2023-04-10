<script setup lang="ts">
    import { reactive } from 'vue';

    const inc = reactive({ count: 0 })

    function increment() {
        inc.count++;
    }

</script>
<template>
    <button class="p-6 max-w-sm mx-auto rounded-full shadow-lg flex items-center font-semibold hover:text-white active:bg-violet-700" @click="increment">
        increase the value
    </button>
    <p>{{ inc.count }}</p>
    
</template>
<style>

</style>