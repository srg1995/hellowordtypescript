<template>
  <div>
    <input type="text" v-model="message" />
    <p>PRECIO: {{ message }}</p>
    <p>IVA :{{ reverse }}</p>
  </div>
</template>

<script lang="ts" setup>
import { Ref, ref, computed, ComputedRef } from "vue";
const IVA = 0.21;
let message: Ref<number> = ref(0);
let reverse: ComputedRef<number> = computed(() => {
  const iva = message.value * IVA;
  return iva;
});
</script>

<style scoped></style>
