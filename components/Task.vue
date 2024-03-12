<template>
  <div class="task">
    <h3>{{ name }}</h3>
    <br>
    <p>Создано: {{ time }}</p>
    <p>Приоритет: {{ priority }}</p>
    <p>Отметки: {{ marks }}</p>
  </div>
</template>

<script setup lang="ts">
  defineProps<{
    name: String,
    time: String,
    priority: String,
    marks: String
  }>()
</script>

<style scoped>
  .task {
    background-color: #FFFFFF;
    border: 2px solid #EEEEEE;
    margin: 2vh;
    padding: 2vh;
    cursor: pointer;
  }
</style>