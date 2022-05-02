<template>
  <button @click="onClick()" :style="{background: color}" class="btn">{{ text }}</button>
</template>

<script>
export default {
  name: "TodoButton",
  props: {
    text: {
      type: String,
      default: "Add Task",
    },
    color: {
      type: String,
      default: "black",
    },
  },
  methods: {
    onClick() {
      console.log('click')
    }
  }
  // props: {
  //   title: String
  // }
  //props: ['title']
};
</script>

<style scoped>
.btn {
  padding: 16px 32px;
  color: #fff;
  border-radius: 8px;
  font-size: 18px;
}
</style>