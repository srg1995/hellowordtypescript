<template>
  <div>
    <h1>Services</h1>
    <PostListWithServiceData />
  </div>
  <div>
    <h1>Directivas personalizadas</h1>
    <p v-custom-size:sm>Directiva 1</p>
    <p v-custom-size:md>Directiva 2</p>
    <p v-custom-font.lg.blue>Directiva 3</p>
  </div>
  <ComputerExample />

  <PostList />
  <ModelForm />
  <ClassBind />
  <ExampleFor />
  <ExampleSelective />
  <h1>Listado de post</h1>
  <PostContainer />

  <CounterOption />
  <CounterComposition />
</template>

<script lang="ts" setup>
import PostContainer from "./components/PostContainer.vue";
import CounterOption from "./components/CounterOption.vue";
import CounterComposition from "./components/CounterComposition.vue";
import ExampleSelective from "./components/ExampleSelective.vue";
import ExampleFor from "./components/ExampleFor.vue";
import ClassBind from "./components/ClassBind.vue";
import ModelForm from "./components/ModelForm.vue";
import PostList from "./components/PostList.vue";
import ComputerExample from "./components/ComputerExample.vue";
import PostListWithServiceData from "./components/PostListWithServiceData.vue";
</script>

<style></style>
