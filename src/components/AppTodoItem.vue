<template>
  <li class="todo-item" :class="{'todo-item--done': todo.completed}">
    <div class="todo-item__status">
      <i class="bi bi-check2"></i>
    </div>
    <span class="todo-item__text">{{ todo.text }}</span>
    <button class="todo-item__remove-button">
      <i class="bi bi-trash3"></i>
    </button>
  </li>
</template>

<script lang="ts">
import { defineComponent, PropType } from "vue";

export default defineComponent({
  props: {
    todo: {
      type: Object as PropType<{
        id:number,
        text: string,
        completed: boolean
      }>,
      required: true
    },
  },
});
</script>
