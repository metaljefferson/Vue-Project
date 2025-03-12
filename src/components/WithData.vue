<template>
    <div>
        <h1>componente com dados</h1>
        <p>Nome: {{ nomeProduto }} - {{ codigoProduto }}</p>
    </div>
</template>

<style scoped>
div {
    text-align: center;
    border: 2px solid rgb(10, 69, 4);
    background-color: #050d04;
    border-radius: 15px;
    margin: 30px;
    padding: 10px;
}

p {
    font-size: 1.2rem;
}
</style>


<script setup>
const nomeProduto = 'Caderno'
const codigoProduto = '#123'
</script>

<!-- <script>
options API

export default {
    data(){
        return {
            nomeProduto: 'Caderno',
            codigoProduto: '#123'
        }
    }
}

Composition API
export default {
    setup(){
        const nomeProduto = 'Caderno'
        const codigoProduto = '#123'

        return {
            nomeProduto,
            codigoProduto
        }
    }
}
</script> -->