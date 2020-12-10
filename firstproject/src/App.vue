<template>
  <div id="app">
    <TodoList v-bind:todos="todos" v-on:delete-todo="deleteTodo"/>
  </div>
</template>

<script>
import TodoList from './components/ToDoList.vue'

export default {
  name: 'app',
  data(){
    return {
      todos: ['Зарядка', 'Завтрак', 'Завтрак', 'Завтрак']
    }
  },
  components: {
    TodoList
  },
  methods: {
    deleteTodo(index){
      this.todos.splice(index, 1);
    }
  }
}
</script>

<style>

</style>