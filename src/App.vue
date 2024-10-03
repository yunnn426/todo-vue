<script setup>
import HelloWorld from './components/HelloWorld.vue'
import TodoList from './components/TodoList.vue'

const tasks = ['운동하기', '밥 먹기', '공부하기공부하기공부하기공부하기공부하기공부하기공부하기공부하기']
</script>

<template>
  <TodoList v-bind:tasks="tasks"/>
  <!-- <div>
    <a href="https://vitejs.dev" target="_blank">
      <img src="/vite.svg" class="logo" alt="Vite logo" />
    </a>
    <a href="https://vuejs.org/" target="_blank">
      <img src="./assets/vue.svg" class="logo vue" alt="Vue logo" />
    </a>
  </div>
  <HelloWorld msg="Vite + Vue" /> -->
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
