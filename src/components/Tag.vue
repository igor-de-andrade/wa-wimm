<script setup lang="ts">
import { defineProps } from 'vue';

const props = defineProps({
  text: String,
});

</script>

<template>

    <span class="tag">
        {{ text }}
    </span>

</template>

<style scoped>

.tag {
    border-style: solid;
    border-width: 1px;
    padding: 5px 10px 5px 10px;
    font-family: "Montserrat", sans-serif;
    font-size: 12px;
    border-radius: 8px;
}


.is-positive {
    background-color: rgb(150, 228, 150);
    color: green;
    border-color: green;
}

.is-negative {
    background-color: rgb(231, 168, 168);
    color: rgb(97, 9, 9);
    border-color: rgb(97, 9, 9);
}

.is-blue {
    background-color: rgb(146, 146, 245);
    color: rgb(14, 14, 102);
    border-color: rgb(14, 14, 102);
}

.is-yellow {
    background-color: rgb(226, 226, 149);
    color: rgb(150, 150, 52);
    border-color: rgb(150, 150, 52);
}

</style>