<template>
  <section class="tasks">
    <TodoTask @delete-task="$emit('delete-task', task.id)" :key="task.id" v-for="task in tasks" :task="task" />
  </section>
</template>

<script>
import TodoTask from "./TodoTask.vue";
export default {
  name: "TodoTasks",
  props: {
    tasks: {
      type: Array,
    },
  },
  components: {
    TodoTask,
  },
  emits: ['delete-task']
};
</script>
