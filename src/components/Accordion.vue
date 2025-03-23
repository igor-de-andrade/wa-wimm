<script setup lang="ts">

import Tag from "./Tag.vue";

import { ref } from "vue";

const isOpen = ref(false);

const togglePanel = () => {
  isOpen.value = !isOpen.value;
}

</script>

<template>
    <div class="component">
        <button class="accordion" @click="togglePanel" :class="{active : isOpen}">
            <span>20/09/2025</span>
            <div class="right-options">
                <Tag class="is-positive" text="+ R$ 5198,59" />

                <i class="fas fa-chevron-down" :class="{ rotated: isOpen }"></i>
            </div>
        </button>
        <div class="panel" :class="{ open: isOpen }">
            <div class="content">
                <div class="info">
                    <Tag class="is-blue" text="Transporte" />
                    <span>Uber do trabalho para casa</span>                   
                </div>
                <div class="details">
                    <Tag class="is-negative" text="- R$ 18,26" />
                    <i class="fas fa-edit"></i>
                    <i class="fas fa-trash"></i>
                </div>
            </div>
            

            <div class="content">
                <div class="info">
                    <Tag class="is-blue" text="Transporte" />
                    <span>Uber do trabalho para casa</span>                   
                </div>
                <div class="details">
                    <Tag class="is-negative" text="- R$ 18,26" />
                    <i class="fas fa-edit"></i>
                    <i class="fas fa-trash"></i>
                </div>
            </div>
            

            <div class="content">
                <div class="info">
                    <Tag class="is-yellow" text="Investimentos" />
                    <span>Jogo do tigrinho</span>                   
                </div>
                <div class="details">
                    <Tag class="is-positive" text="+ R$ 5262,26" />
                    <i class="fas fa-edit"></i>
                    <i class="fas fa-trash"></i>
                </div>
            </div>
        </div>
    </div>
</template>

<style scoped>

.component {
    border-style: solid;
    border-width: 1px;
    border-radius: 4px;
    border-color: #e0d6d6;
}

.accordion {
    display: flex;
    justify-content: space-between;
    background-color: #ffffff;
    color: #444;
    cursor: pointer;
    padding: 10px 18px;
    width: 100%;
    font-family: "Montserrat", sans-serif;
    font-size: 14px;
    align-items: center;
    border: none;
    border-radius: 4px;
    transition: 0.4s;
}

.right-options {
    display: flex;
    gap: 20px;
    align-items: center;
}

.active {
  /* background-color: #cfe2ff; */
  background-color: rgb(235, 179, 235);
  border-bottom-left-radius: 0;
  border-bottom-right-radius: 0;
}

.panel {
    background-color: #ffffff;
    overflow: hidden; /* Garante que o conteúdo não fique visível antes da abertura */
    max-height: 0; /* Impede que o painel apareça antes de abrir */
    opacity: 0; /* Deixa o painel invisível no início */
    padding: 0 18px; /* Remove o padding inicial para evitar um efeito de salto */
    transition: max-height 0.4s ease-in-out, opacity 0.3s ease-in-out, padding 0.3s ease-in-out;
    display: flex;
    flex-direction: column;
    gap: 10px;
}

/* Painel aberto */
.panel.open {
    max-height: 500px; /* Define um valor alto para permitir expansão (ajuste conforme necessário) */
    opacity: 1; /* Torna o painel visível */
    padding: 16px 18px; /* Restaura o padding quando aberto */
    border-bottom-left-radius: 4px;
    border-bottom-right-radius: 4px;
}

.accordion i {
    transition: transform 0.3s ease-in-out; /* Garante a transição suave */
}

.rotated {
    transform: rotate(-180deg);
}

.content {
    display: flex;
    flex-direction: row;
    justify-content: space-between;
    gap: 10px;
    align-items: center;
}

.info {
    display: flex;
    flex-direction: row;
    gap: 10px;
    align-items: center;
    font-family: "Montserrat", sans-serif;
    font-size: 14px;
}

.details {
    display: flex;
    flex-direction: row;
    gap: 20px;
    align-items: center;
}


</style>