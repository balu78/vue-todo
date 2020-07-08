<template>
  <div id="app">
    <Todos v-bind:todos="todos" v-on:del-todo="deleteTodo"/>
  </div>
</template>

<script>
import Todos from './components/Todos'
export default {
  name: 'App',
  components: {
    Todos
  },
  data() {
    return {
      todos: [
        {
          id: 1,
          title: "todo 1",
          complete: true
        },
        {
          id: 2,
          title: "todo 2",
          complete: false
        },
        {
          id: 3,
          title: "todo 3",
          complete: false
        }
      ]
    }
  },
  methods:{
    deleteTodo(id){
      this.todos = this.todos.filter(todo => todo.id != id);
    }
  }
}
</script>

<style>

</style>
