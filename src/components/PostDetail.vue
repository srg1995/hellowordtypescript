<template>
  <div class="post">
    <h1>{{ title }}</h1>
    <p>{{ content }}</p>
    <input type="text" v-model="message" />
    <button @click="handleClick">Di hola</button>
  </div>
</template>

<script lang="ts" setup>
import { defineProps, defineEmits, Ref, ref } from "vue";
const props = defineProps({
  title: String,
  content: String,
});
const emit = defineEmits(["sayHi"]);
const handleClick = () => {
  emit("sayHi", message.value);
};
let message: Ref<string> = ref("");
</script>

<style scoped>
.post {
  width: 200px;
  height: 200px;
  background-color: red;
  border-radius: 25px;
  margin: 15px;
  padding: 15px;
}
</style>
