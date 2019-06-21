<template>
  <div>
    <h1>Todo List</h1>
    <Todo :todos="todoList" @removeTodo="appDeleteTodo" />
  </div>
</template>
<script>
import Todo from "@/components/Todo.vue";

export default {
  data() {
    return {
      todoList: ["Walk the dogs", "Go for a ride"]
    };
  },
  components: {
    Todo
  },
  methods: {
    appDeleteTodo(index) {
      this.todoList.splice(index, 1);
    }
  }
};
</script>
