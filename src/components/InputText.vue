<script setup lang="ts">
import Label from './Label.vue';

const props = defineProps({
  label: String,
})

</script>

<template>
    <div class="input-text">
        <Label v-text="label" />
        <input type="text" class="form-control">
    </div>
</template>

<style scoped>

.input-text {
    width: 100%;
}

</style>