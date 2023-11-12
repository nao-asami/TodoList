<template>
  <v-row class="ma-5">
    <v-list>
      <v-list-item v-for="todo in todoList" :key="todo.id" :title="todo.title" :subtitle="todo.detail" />
    </v-list>
  </v-row>
</template>

<script setup lang="ts">
import { ref } from 'vue'

const todoList = ref([
  { id:1, title:"Todo1", detail: "TodoTodoTodo1", done: false },
  { id:2, title:"Todo2", detail: "TodoTodoTodo2", done: false },
  { id:3, title:"Todo3", detail: "TodoTodoTodo3", done: true },
  { id:4, title:"Todo4", detail: "TodoTodoTodo4", done: false }
]);
</script>
