<script setup>
import FirstComponent from './components/FirstComponent.vue'
import WithData from './components/WithData.vue'
import WithPrimitiveReactiveData from './components/WithPrimitiveReactiveData.vue'
import WithNotPrimitiveReactiveData from './components/WithNotPrimitiveReactiveData.vue'

</script>

<template>
  <header>Vue</header>
  <WithNotPrimitiveReactiveData />
  <WithPrimitiveReactiveData />
  <WithData />
  <FirstComponent />
</template>

<style scoped></style>
