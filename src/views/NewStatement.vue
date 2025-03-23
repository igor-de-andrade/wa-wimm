<script setup lang="ts">
import Button from '../components/Button.vue';
import InputDate from '../components/InputDate.vue';
import InputDecimal from '../components/InputDecimal.vue';
import InputText from '../components/InputText.vue';
import Select from '../components/Select.vue';

import { defineEmits } from 'vue';

const emit = defineEmits<{
  (e: 'close'): void;
}>()

const closeStatement = () => {
  emit('close');
};

</script>

<template>
    <form class="form new-statement">
        <div class="form-row">
            <InputDate label="Data" />
            <Select label="Tipo" />
            <InputDecimal label="Valor" />
            <Select label="Categoria" />
        </div>
        <div class="form-row">
            <InputText label="Descrição" />
        </div>
        <div class="form-row form-buttons">
            <Button class="primary" text="Adicionar" />
            <Button class="secundary" text="Fechar" @click="closeStatement" />
        </div>
    </form>
</template>

<style scoped>

.new-statement {
    display: flex;
    flex-direction: column;
    gap: 20px;
    padding: 20px;
    border-style: solid;
    border-width: 1px;
    border-color: #e0d6d6;
    border-radius: 4px;
    box-shadow: 4px 4px 15px 5px rgba(0, 0, 0, 0.3); /* Sombra com expansão */
}

.form-row {
    display: flex;
    flex-direction: row;
    gap: 20px;
}

.form-buttons {
    justify-content: right;
}

</style>