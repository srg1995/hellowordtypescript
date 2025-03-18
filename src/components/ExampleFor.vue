<template>
  <ul>
    <li v-for="country in countries" v-bind:key="country">{{ country }}</li>
  </ul>

  <ul>
    <li v-for="country in countries2" v-bind:key="country.code">
      {{ country.name }}
    </li>
  </ul>
</template>

<script lang="ts" setup>
interface ICountry {
  code: string;
  name: string;
}
import { ref, Ref } from "vue";
let countries: Ref<Array<string>> = ref(["Spain", "France", "Germany"]);
let countries2: Ref<Array<ICountry>> = ref([
  { code: "es", name: "spain" },
  { code: "fr", name: "france" },
]);
</script>

<style></style>
