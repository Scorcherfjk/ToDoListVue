<template>
  <li>{{ todo.text }}</li>
</template>

<script>
export default {
  name: 'ToDoList',
  props: {
    todo: Object
  }
}
</script>

<style>

</style>