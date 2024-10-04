<script setup>
import TodoList from './components/TodoList.vue'

const tasks = ['운동하기', '밥 먹기', 'hello hello hello ✅🩵🥹💌!']
</script>

<template>
  <TodoList v-bind:tasks="tasks"/>
</template>

<style scoped>

.logo {
  height: 6em;
  padding: 1.5em;
  will-change: filter;
  transition: filter 300ms;
}
.logo:hover {
  filter: drop-shadow(0 0 2em #646cffaa);
}
.logo.vue:hover {
  filter: drop-shadow(0 0 2em #42b883aa);
}
</style>
