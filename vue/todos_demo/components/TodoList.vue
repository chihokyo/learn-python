<template>
  <div>
    <h2>TodoList</h2>
    <ul>
      <!-- <TodoItem
        v-for="(todo, index) in todos"
        :key="index"
        :todo="todo"
        :index="index"
        :deleteTodo="deleteTodo"
      ></TodoItem>-->
      <!-- 使用Pubsub订阅消息 -->
      <TodoItem v-for="(todo, index) in todos" :key="index" :todo="todo" :index="index"></TodoItem>
    </ul>
  </div>
</template>

<script>
import TodoItem from "./TodoItem";
export default {
  props: {
    todos: Array,
    deleteTodo: Function,
  },
  components: {
    TodoItem,
  },
};
</script>

<style>
</style>