<template>
    <div class="componente">
        <h1>Componente com data binding</h1>
        <!-- <input type="text" v-bind:value="valor" /> -->
        <p>{{ valor }}</p>
        <!-- <input type="text" v-bind:value="valor" v-on:input="(e) => valor = e.target.value" /> -->
        <!-- <input type="text" :value="valor" @input="(e) => valor = e.target.value" /> -->
        <input type="text" v-model="valor" />
    </div>
</template>

<script setup>

import { ref } from 'vue'

const valor = ref("Vue 3")

</script>