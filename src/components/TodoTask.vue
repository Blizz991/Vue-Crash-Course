<template>
    <article  :class="[task.reminder ? 'reminder' : '', 'tasks__task']">
      <h3>
          {{ task.text }}
        <i class="fas fa-times"></i>
      </h3>
      <p>{{task.day}}</p>
    </article>
</template>

<script>
export default {
  name: "TodoTask",
  props: {
    task: Object,
  },
};
</script>

<style scoped>
.tasks__task {
    background: #f4f4f4;
    margin: 10px 0;
    padding: 10px 20px;
    cursor: pointer;
}

h3 {
    display: flex;
    justify-content: space-between;
}

.fas {
    color: red;
    font-size: 28px;
}

.reminder {
    border-left: 6px solid green;
}
</style>