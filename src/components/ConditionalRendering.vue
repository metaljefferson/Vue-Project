<template>
    <div class="componente">
        <h1>Componente com renderizacao condicional</h1>
        <p>Nome: {{ nome }}</p>
        <p v-if="qtdeCachorros === 0">Nao tem cachorros</p>
        <p v-else-if="qtdeCachorros === 1">Tem um cachorro</p>
        <p v-else>tem muitos cachorros</p>
    </div>
</template>

<script setup>

import { defineProps } from 'vue';

defineProps({
    nome: String,
    qtdeCachorros: Number
});
</script>