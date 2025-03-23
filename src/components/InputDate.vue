<script setup lang="ts">
import Label from './Label.vue';

const props = defineProps({
  label: String,
})

</script>

<template>
    <div class="input-date">
        <Label v-text="label" />
        <input type="date" class="form-control">
    </div>
</template>

<style scoped>

.input-date {
    width: 100%;
}

</style>