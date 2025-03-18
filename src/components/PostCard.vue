<template>
  <div class="post-card">
    <h3>Titulo</h3>
    <p>
      Lorem ipsum dolor sit amet consectetur, adipisicing elit. Laboriosam, illo
      expedita sit pariatur quaerat ducimus quo architecto nisi, officiis
      assumenda ipsum, provident ad. Possimus quasi saepe vel illo soluta iste?
    </p>
    <PostButton />
  </div>
</template>
<script lang="ts" setup>
import PostButton from "./PostButton.vue";
</script>
<style scoped>
.post-card {
  border-radius: 15px;
  padding: 10px;
  margin: 5px;
  border: 1px solid #ccc;
}
</style>
