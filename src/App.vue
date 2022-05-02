<template>
  <div id="app">
    <main class="container">
      <TodoHeader />
      <TodoTasks :tasks="tasks" />
    </main>
  </div>
</template>

<script>
import TodoHeader from "./components/TodoHeader.vue";
import TodoTasks from "./components/TodoTasks.vue";

export default {
  name: "App",
  components: {
    TodoHeader,
    TodoTasks,
  },
  data() {
    return {
      tasks: [],
    };
  },
  created() {
    this.tasks = [
      {
        id: 1,
        text: "Doctors Appointment",
        day: "March 1st at 2:30pm",
        reminder: true,
      },
      {
        id: 2,
        text: "Meeting at School",
        day: "March 3rd at 1:30pm",
        reminder: true,
      },
      {
        id: 3,
        text: "Food Shopping",
        day: "March 3rd at 11:00am",
        reminder: false,
      },
    ];
  },
};
</script>

<style>
body {
min-height: 100vh;
margin: 0;
}
</style>

<style scoped>
div {
  display: flex;
  align-items: center;
  justify-content: center;
  min-height: 100vh;
}
.container {
  width: 400px;
  margin: auto;
}
</style>
