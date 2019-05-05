<template>
<div class="todo-wrapper">
  <TodoItem v-for="(todoItem,index) in todoList" :key="index" :todoItem="todoItem"/>
</div>
</template>

<script>
import TodoItem from "./TodoItem";

export default {
  name: "TodoList",
  props: {
    todoList: Array
  },
  components: {
    TodoItem
  },
};
</script>

<style scoped>
.todo-wrapper{
    display: flex;
}
</style>