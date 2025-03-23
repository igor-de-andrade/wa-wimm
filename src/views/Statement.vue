<script setup lang="ts">
import Accordion from '../components/Accordion.vue';
import Button from '../components/Button.vue';
import MonthDatePicker from '../components/MonthDatePicker.vue'
import NewStatement from './NewStatement.vue';
import { ref } from 'vue';

const showNewStatement = ref(false);

</script>

<template>

<div class="extrato">


    <div class="options">
        <div class="buttons">
            <Button class="primary" text="Incluir movimentação" @click="showNewStatement = true" />
        </div>
        <div class="filters">
            <MonthDatePicker />
        </div>
    </div>

    <NewStatement v-if="showNewStatement" @close="showNewStatement = false" />

    <Accordion />
    <Accordion />
  </div>

</template>

<style scoped>

.extrato {
  display: flex;
  flex-direction: column;
  margin: 5%;
  gap: 10px;
}

.options {
  display: flex;
  flex-direction: row;
  justify-content: space-between;
}

</style>