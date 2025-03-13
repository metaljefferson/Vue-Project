<template>
    <div class="componente">
        <h1>Componente que escuta evento</h1>
        <p>Total: R$ {{ total }}</p>
        <div class="list">
            <EmitsEvent item="Item1" :preco="1.99" @foiAdicionado="atualizarTotal"/>
            <EmitsEvent item="Item2" :preco="2.99" @foiAdicionado="atualizarTotal"/>
            <EmitsEvent item="Item3" :preco="3.99" @foiAdicionado="atualizarTotal"/>
        </div>
    </div>
</template>

<script setup>
import EmitsEvent from './EmitsEvent.vue';
import { ref } from 'vue';

const total = ref(0);

function atualizarTotal(p){
    const valor = total.value + p;
    total.value = +valor.toFixed(2);
}
</script>

<style scoped>

.list {
    display: flex;
    justify-content: space-between;
}
</style>