<script setup>
import Header from "./components/Header.vue";
import Form from "./components/Form.vue";
import List from "./components/List.vue";
import { reactive } from "vue";

const state = reactive({
  tasks: [],
  lastTaskId: 0,
  filter: "all",
});

function getTasks(filter) {
  const { tasks } = state;
  if (filter === "pending") {
    const pendingTasks = tasks.filter(task => !task.isComplete);
    return pendingTasks;
  } else if (filter === "completed") {
    const completedTasks = tasks.filter(task => task.isComplete);
    return completedTasks;
  }

  return tasks;
}

function changeTask(task) {
  task.isComplete = !task.isComplete;
}

function registerTask({target}) {
  state.lastTaskId++;
  const task = {title: target.value, isComplete: false, id: state.lastTaskId};
  state.tasks.push(task);
}

</script>

<template>
  <Header :pendingTasks="getTasks('pending')"></Header>
  <Form :state="state" :register="registerTask"></Form>
  <List :tasks="getTasks(state.filter)" :change="changeTask"></List>
</template>

<style scoped></style>
