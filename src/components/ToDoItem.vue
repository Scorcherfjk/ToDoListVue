<template>
  <li>
    {{ todo.text }}
    <button v-on:click="deleteItem">&times;</button>
  </li>
</template>

// ! LLAMADA
<!-- <ol>
  <ToDoItem 
    v-for="todo in todos"
    v-bind:todo="todo"
    v-bind:key="todo.id">
  </ToDoItem>
</ol> -->
// import ToDoItem from './components/ToDoItem';

<script>
export default {
  name: 'ToDoItem',
  props: {
    todo: Object
  },
  methods:{
    deleteItem(){
      console.log(this.todo.id);
    }
  }
}
</script>

<style>

</style>