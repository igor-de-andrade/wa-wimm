<script setup lang="ts">

import { defineProps } from 'vue';

const props = defineProps({
  text: String,
})


</script>

<template>

    <label class="label">
        {{  text }}
    </label>

</template>

<style scoped>

.label {
  font-size: 16px;
}

</style>