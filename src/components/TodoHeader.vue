<template>
  <header>
    <h1>{{ title }}</h1>
    <TodoButton text="Add task" color="green" />
    <!-- <TodoButton text="Update task" color="blue" />
    <TodoButton text="Delete task" color="red" /> -->
  </header> 
</template>

<script>
import TodoButton from "./TodoButton.vue"

export default {
  name: "TodoHeader",
  props: {
    title: {
      type: String,
      default: 'Task Tracker',
    }
  },
  components: {
    TodoButton,
  },
  // props: {
  //   title: String
  // }
  //props: ['title']
}
</script>

<style scoped>
header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  margin-bottom: 20px;
}
</style>