<template>
  <div id="app">
    <AppHeader/>
    <AppFilters/>

    <main class="app-main">
      <AppTodoList/>

      <AppAddTodo/>
    </main>

    <AppFooter/>
  </div>
</template>

<script lang="ts">
import { defineComponent } from "vue";
import AppHeader from "./components/AppHeader.vue"
import AppFilters from "./components/AppFilters.vue"
import AppTodoList from "./components/AppTodoList.vue"
import AppAddTodo from "./components/AppAddTodo.vue"
import AppFooter from "./components/AppFooter.vue"
export default defineComponent({
  components:{
    AppHeader,
    AppFilters,
    AppTodoList,
    AppAddTodo,
    AppFooter
  }
})
</script>
