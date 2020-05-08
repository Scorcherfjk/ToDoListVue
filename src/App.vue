<template>
  <div id="app">
    <h1>ToDo List with Vue</h1>
    <div class="container">
      <div class="inputItem">
        <input type="text" v-model="message">
        <button v-on:click="addToDo">➕</button>
      </div>
      <ol>
        <li v-for="todo in todos" v-bind:key="todo.id">
          <span>{{ todo.id + '. ' + todo.text }}</span>
          <div class="editItem">
            <button v-on:click="updateItem(todo.id)">⭕</button>
            <button v-on:click="deleteItem(todo.id)">❌</button>
          </div>
        </li>
      </ol>
    </div>
  </div>
</template>

<script>
import './assets/sass/app.sass'

export default {
  name: 'App',
  data(){
    const app = {
      message: '',
      todos: [
      ]
    }
    return app;
  },
  methods:{
    addToDo(){
      if (this.message) {
        this.todos.push({ id: this.todos.length, text: this.message });
        this.message = '';
      }
    },
    deleteItem(id){
      this.todos = this.todos.filter(e => e.id != id)
    },
    updateItem(id){
      const idx = this.todos.findIndex(e => e.id == id)
      this.todos[idx].text = prompt('ingresa un nuevo texto', this.todos[idx].text)
    }
  }
}
</script>

<style lang="sass">

</style>
