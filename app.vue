<template>
  <div class="app">  
    <div v-for="post in posts" :key = "post.id">
      <Task :name="post.name" :time="post.time" :priority="post.priority" :marks="post.marks" />
    </div>
  </div>
</template>

<script setup lang="ts">
// const posts = [
//   {id: 1, name: 'Тестовая задача №1', time: 'только что', priority: 'normal', marks: 'design, development'},
//   {id: 2, name: 'Тестовая задача №2', time: 'только что', priority: 'normal', marks: 'design, development'},
//   {id: 3, name: 'Тестовая задача №3', time: 'только что', priority: 'normal', marks: 'design, development'},
// ] 
import { onMounted, ref } from 'vue';
const posts = ref([]);

onMounted(async () => {
  try {
    const res = await fetch("http://localhost:3001/posts");
    posts.value = await res.json();
  } catch (err) {
    console.log(err);
  }
});

</script>

<style>
* {
  margin: 0;
  padding: 0;
}
</style>