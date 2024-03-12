<template>
  <form class="formAdd">
    <p>НАЗВАНИЕ ЗАДАЧИ</p>
    <input />
    <p>ПРИОРИТЕТ</p>
    <select>
      <option value="low">Low</option>
      <option value="normal">Normal</option>
      <option value="high">High</option>
    </select>
    <p>ОТМЕТКИ</p>
    <select>
      <option value="research">Research</option>
      <option value="design">Design</option>
      <option value="development">Development</option>
    </select>
    <p>ОПИСАНИЕ</p>
    <textarea></textarea>
  </form>
</template>

<script lang="ts" setup>

</script>

<style scoped>
  .formAdd {
    background-color: #FFFFFF;
    border: 2px solid #EEEEEE;
    margin: 2vh;
    padding: 2vh;
  }
</style>