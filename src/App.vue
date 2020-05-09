<template>
  <div>
    <ToDoList></ToDoList>
    <ToDoList></ToDoList>
    <ToDoList></ToDoList>
  </div>
</template>

<script>
import ToDoList from './components/ToDoListComplete';

export default {
  name: 'App',
  components:{
    ToDoList
  }
}
</script>

<style lang="sass">

</style>
