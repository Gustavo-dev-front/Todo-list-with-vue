<script setup>
const { tasks, change } = defineProps(["tasks", "change"]);
</script>

<template>
  <ul class="List list-group container px-3 p-0">
    <li v-for="task in tasks" class="list-group-item d-flex align-items-center gap-2" :class="{ done: task.isComplete }" @click="change(task)">
      <input type="checkbox" :id="task.id" :checked="task.isComplete">
      <label class="label" :for="task.id">{{ task.title }}</label>
    </li>
  </ul>
</template>

<style scoped>
.done {
  text-decoration: line-through;
}

.label {
  pointer-events: none;
}
</style>