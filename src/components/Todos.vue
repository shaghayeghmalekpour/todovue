<template>
<div>
  <div v-for="todo in todos" v-bind:key="todo.id">
    <TodoItem v-bind:todo="todo" v-on:del-todo="$emit('del-todo' ,
              todo.id)" />
  </div>
</div>
</template>

<script>
//chera az model address ke be compo eshare kard irad gereft?
import TodoItem from "./TodoItem.vue";

export default {
  name: "Todos",
  components: {
    TodoItem
  },
  props: ['todos']
}
</script>

<style scoped>

</style>