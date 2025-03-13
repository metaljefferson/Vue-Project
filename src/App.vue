<script setup>
import FirstComponent from './components/FirstComponent.vue'
import WithData from './components/WithData.vue'
import WithPrimitiveReactiveData from './components/WithPrimitiveReactiveData.vue'
import WithNotPrimitiveReactiveData from './components/WithNotPrimitiveReactiveData.vue'
import DateBinding from './components/DateBinding.vue'
import WithProps from './components/WithProps.vue'
import ListenEvent from './components/ListenEvent.vue'
import ComputedProperties from './components/ComputedProperties.vue'
import AssistedProperties from './components/AssistedProperties.vue'
import ConditionalRendering from './components/ConditionalRendering.vue'
import RenderingList from './components/RenderingList.vue'
import Slots from './components/Slots.vue'

const borracha = 'borracha'
const precoBorracha = 50.90

const cachorrosDoJoao = [
  { nome: 'Rex', idade: 5 },
  { nome: 'Toto', idade: 2 },
  { nome: 'Bilu', idade: 10 }
]
</script>

<template>
  <header>Vue</header>
  <Slots>
    <template v-slot:icone>
      <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none"
        stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"
        class="icon icon-tabler icons-tabler-outline icon-tabler-home">
        <path stroke="none" d="M0 0h24v24H0z" fill="none" />
        <path d="M5 12l-2 0l9 -9l9 9l-2 0" />
        <path d="M5 12v7a2 2 0 0 0 2 2h10a2 2 0 0 0 2 -2v-7" />
        <path d="M9 21v-6a2 2 0 0 1 2 -2h2a2 2 0 0 1 2 2v6" />
      </svg>
    </template>

    <template v-slot:texto>
      Home
    </template>
   
  </Slots>
  <RenderingList nome="Joao" :cachorros="cachorrosDoJoao" />
  <ConditionalRendering nome="Maria" :qtdeCachorros="2" />
  <AssistedProperties />
  <ComputedProperties />
  <ListenEvent />
  <WithProps :item="borracha" :preco="precoBorracha" />
  <DateBinding />
  <WithNotPrimitiveReactiveData />
  <WithPrimitiveReactiveData />
  <WithData />
  <FirstComponent />
</template>

<style scoped></style>
