<template>
  <section class="add-todo">
    <form v-if="isFormVisible" class="add-todo__form">
      <button class="close-button" type="button" @click="showForm">
        <i class="bi bi-x"></i>
      </button>
      <div class="text-input text-input--focus">
        <input class="input" />
      </div>
      <button class="button button--filled">Add task</button>
    </form>
    <button v-else @click="showForm" class="add-todo__show-form-button">
      <i class="bi bi-plus-lg"></i>
    </button>
  </section>
</template>

<script lang="ts">
import { defineComponent } from "vue";

interface State {
  isFormVisible: boolean
}

export default defineComponent({
  data(): State {
    return {
      isFormVisible: false
    }
  },
  methods:{
    showForm(){
      this.isFormVisible = !this.isFormVisible
    }
  }
})
</script>
