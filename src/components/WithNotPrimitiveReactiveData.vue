<template>
    <div class="componente">
        <h1>componente com dados reativos Nao Primitivos</h1>
        <p>Nome: {{pessoa.nome }} | Idade: {{ pessoa.idade }}</p>
        <button @click="fazerAniversario()">Fazer Aniversario</button>
        <button @click="mudarNome()">Mudar Nome</button>
    </div>
</template>

<!-- <script setup>
import { reactive } from 'vue'

const pessoa = reactive({
    nome: "ana",
    idade: 20
})


function fazerAniversario() {
    pessoa.idade += 1

}

function mudarNome() {
    pessoa.nome = "joao"
}
</script> -->

<script>
export default{
    data(){
        return{
            pessoa: {
                nome: "ana",
                idade: 20
            }
        }
    },

    methods:{
        fazerAniversario(){
            this.pessoa.idade += 1
        },
        mudarNome(){
            this.pessoa.nome = "joao"
        }
    }
}

</script>

<!-- V-on e @click são a mesma coisa, mas @click é mais utilizado por ser mais simples e direto. -->