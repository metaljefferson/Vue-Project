<template>
    <div class="componente">
        <h1>Componente com renderizacao Lista</h1>
        <p>Nome: {{ nome }}</p>
        <p v-show="cachorros.length === 0">Nao tem cachorro</p>
        <ul>
            <li v-for="cachorro in cachorros" :key="cachorro.id">
                Nome: {{ cachorro.nome }} | Idade: {{ cachorro.idade }}
            </li>
        </ul>
    </div>
</template>

<script setup>

import { defineProps } from 'vue';

defineProps({
    nome: String,
    cachorros: Array
});
</script>

<style scoped>
ul {
    margin: 0;
    padding: 0px;
}

li {
    list-style: none;
    text-align: center;
    font-size: large;
}
</style>