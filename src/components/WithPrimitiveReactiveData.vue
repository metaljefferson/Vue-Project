<template>
    <div class="componente">
        <h1>componente com dados reativos Primitivos</h1>
        <p>Nome: {{ nome }} | Idade: {{ idade }}</p>
        <button v-on:click="fazerAniversario()">Fazer Aniversario</button>
        <button @click="mudarNome()">Mudar Nome</button>
    </div>
</template>

<script setup>
import { ref } from 'vue'

const nome = ref("ana")
const idade = ref(20)

function fazerAniversario() {
    idade.value += 1

}

function mudarNome() {
    nome.value = "joao"
}
</script>

<!-- V-on e @click são a mesma coisa, mas @click é mais utilizado por ser mais simples e direto. -->