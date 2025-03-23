<script setup lang="ts">
import Label from './Label.vue';

const props = defineProps({
  label: String,
})

</script>

<template>

    <div class="select">
        <Label v-text="label" />
        <select class="form-select">
            <option value="1">Teste</option>
            <option value="1">Testes</option>
        </select>
    </div>

</template>

<style scoped>

.select {
    width: 100%;
}

</style>