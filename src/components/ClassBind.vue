<template>
  <p v-bind:class="{ danger: hasError }">
    El mensaje se ha enviado satisfactoriamente
  </p>
  <p v-bind:style="{ backgroundColor: c }">
    El mensaje se ha enviado satisfactoriamente
  </p>
  <button v-on:click="handleClick">Cambiar color</button>
</template>
<script lang="ts" setup>
import { Ref, ref } from "vue";
let hasError = true;
let c: Ref = ref("#fff");
const handleClick = () => (c.value = "#ff0000");
</script>

<style scoped>
.danger {
  color: red;
}
</style>
