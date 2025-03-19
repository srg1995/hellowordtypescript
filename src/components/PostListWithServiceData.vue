<template>
  <div class="container">
    <ul>
      <li v-for="post in posts" :key="post.id">
        {{ post.title }}
      </li>
    </ul>
  </div>
</template>

<script lang="ts" setup>
import PostService from "@/services/PostService";
import { onMounted } from "vue";

const service = new PostService();
const posts = service.getPosts();

onMounted(async () => {
  await service.fetchAll();
});
</script>

<style scoped>
.container {
  display: flex;
  flex-wrap: wrap;
  flex-direction: row;
  justify-content: space-aroun;
}
ul {
  width: 90%;
  list-style-type: none;
  padding: 10px;
}
li {
  margin: 10px;
  border: solid 1px black;
  padding: 10px;
}
</style>
