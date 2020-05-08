<template>
  <ol>
    <li v-for="todo in todos" v-bind:key="todo.id">
      {{ todo.text }}
      <button v-on:click="deleteItem(todo.id)">&times;</button>
    </li>
  </ol>
</template>

// ! LLAMADA
<!-- <ToDoList v-bind:todos="todos"></ToDoList> -->
// import ToDoList from './components/ToDoList';


<script>
export default {
  name: 'ToDoList',
  props:{
    todos: Array
  },
  methods:{
    deleteItem(id) {
      console.log(this.todos[id].id + '---' + id);
    }
  }
}
</script>

<style>

</style>