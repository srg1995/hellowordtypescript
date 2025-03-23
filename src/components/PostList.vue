<template>
  <div class="container">
    <PostDetail
      v-for="post in info"
      :key="post.title"
      :title="post.title"
      :content="post.content"
      @sayHi="showAlert"
    />
  </div>
</template>

<script lang="ts" setup>
import PostDetail from "./PostDetail.vue";

interface IPost {
  title: string;
  content: string;
}

let info: Array<IPost> = [
  { title: "este es el titulo 1", content: "este es el contenido 1" },
  { title: "este es el titulo 2", content: "este es el contenido 2" },
];
function showAlert(msg: string) {
  alert(msg);
}
</script>

<style scoped>
.container {
  display: flex;
  flex-wrap: wrap;
  flex-direction: row;
  justify-content: space-aroun;
}
</style>
