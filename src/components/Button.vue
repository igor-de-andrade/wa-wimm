<script setup lang="ts">
import { defineProps } from 'vue';

const props = defineProps({
  text: String,
})

</script>

<template>

    <button type="button" class="btn btn-dark">
        {{ text }}
    </button>

</template>

<style scoped>

.primary {
  background-color: rgb(71, 15, 71) !important;
}

.primary:hover {
  background-color: rgb(95, 25, 95) !important;
}

.secundary {
  background-color: rgb(109, 109, 109) !important;
}

.secundary:hover {
  background-color: rgb(150, 150, 150) !important;
}


</style>