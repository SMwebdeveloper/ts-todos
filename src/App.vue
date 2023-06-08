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

<script>
import { defineComponent } from "vue";
import AppHeader from "@/components/AppHeader"
import AppFilters from "@/components/AppFilters"
import AppTodoList from "@/components/AppTodoList"
import AppAddTodo from "@/components/AppAddTodo"
import AppFooter from "@/components/AppFooter"
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
