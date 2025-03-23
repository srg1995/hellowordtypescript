<template>
  <h1 v-if="age > 10">Es mayor de edad</h1>
  <h1 v-else>Es menor de edad</h1>
  <h1 v-show="age > 10">Es mayor de edad</h1>
</template>

<script lang="ts" setup>
let age = 10;
</script>

<style scoped></style>
