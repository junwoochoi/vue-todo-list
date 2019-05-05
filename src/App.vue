<template>
  <div id="app">
    <TodoInput/>
    <TodoList :todoList="todoList"/>
  </div>
</template>

<script>
import TodoList from "./components/TodoList.vue";
import TodoInput from "./components/TodoInput.vue";

export default {
  name: "app",
  components: {
    TodoList,
    TodoInput
  },
  data(){
    return{
      todoList: [
        {
          todo: "할일 들어갈 자리",
          state: "active"
        }
      ]
    }
  }
  
};
</script>

<style>
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
