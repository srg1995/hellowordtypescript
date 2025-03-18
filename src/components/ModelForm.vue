<template>
  <form>
    <input v-model="inputText" type="text" />
    <input type="checkbox" v-model="agree" />Acepto los terminos y condiciones
    <select v-model="country">
      <option value="Spain">Spain</option>
      <option value="France">France</option>
      <option value="Germany">Germany</option>
    </select>
  </form>

  <h3>{{ inputText }}</h3>
</template>

<script lang="ts" setup>
import { Ref, ref } from "vue";
let inputText: Ref<string> = ref("");
let agree: Ref<boolean> = ref(false);
let country: Ref<string> = ref("Germany");
</script>

<style scoped></style>
