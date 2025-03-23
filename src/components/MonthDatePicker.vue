<script setup lang="ts">
import { ref } from "vue";

const currentMonth = ref(new Date().toISOString().slice(0, 7))

</script>

<template>
    <input type="month" v-model="currentMonth" class="form-control">
</template>

<style scoped>
</style>
