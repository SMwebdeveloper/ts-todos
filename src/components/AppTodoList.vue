<template>
  <ul class="todo-list">
    <AppTodoItem
      v-for="todo in todos"
      :key="todo.id"
      :todo="todo"
      @toggle-todo="toggleTodo"
      @remove-todo="removeTodo"
    />
  </ul>
</template>

<script lang="ts">
import { Todo } from "@/types/Todo";
import { defineComponent } from "vue";
import AppTodoItem from "./AppTodoItem.vue";

interface State {
  todos: Todo[];
}
export default defineComponent({
  components: {
    AppTodoItem,
  },
  data(): State {
    return {
      todos: [
        { id: 0, text: "Learn the basics of Typescript", completed: true },
        { id: 1, text: "Subscribe to the channel", completed: false },
        { id: 2, text: "Learn the basics of Typescript", completed: false },
      ],
    };
  },
  methods: {
    toggleTodo(id: number) {
      const targetTodo = this.todos.find((todo) => todo.id === id);

      if (targetTodo) {
        targetTodo.completed = !targetTodo.completed;
      }
    },
    removeTodo(id: number) {
       const todos = this.todos.filter(todo => todo.id !== id)
       this.todos = todos
    },
  },
});
</script>
