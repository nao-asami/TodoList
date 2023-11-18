<template>
  <div class="ma-10">
    <v-row>
      <v-col><v-text-field v-model="todoTitle" /></v-col>
      <v-col><v-text-field v-model="todoDetail" /></v-col>
      <v-col><v-btn @click="addTodo" icon="mdi-plus" /></v-col>
    </v-row>

    <v-row>
      <v-list>
        <v-list-item v-for="todo in todoList" :key="todo.id" :title="todo.title" :subtitle="todo.detail" />
      </v-list>
    </v-row>
  </div>
</template>

<script setup lang="ts">
import { ref } from 'vue'

const todoTitle = ref();
const todoDetail = ref();

const addTodo = function() {
  todoList.value.push({id: 9, title: todoTitle.value, detail: todoDetail.value, done: false  })
}

const todoList = ref([
  { id:1, title:"Todo1", detail: "TodoTodoTodo1", done: false },
  { id:2, title:"Todo2", detail: "TodoTodoTodo2", done: false },
  { id:3, title:"Todo3", detail: "TodoTodoTodo3", done: true },
  { id:4, title:"Todo4", detail: "TodoTodoTodo4", done: false }
]);
</script>
