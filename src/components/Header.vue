<script setup>
import { defineProps } from 'vue';
const {pendingTasks} = defineProps(['pendingTasks']);
</script>


<template>
  <header class="Header container py-5 px-3">
    <h1>Minhas tarefas</h1>
    <span class="fs-6">Você tem <strong>{{pendingTasks.length}}</strong> tarefa{{ pendingTasks.length > 1 ? "s" : ""}} pendente{{ pendingTasks.length > 1 ? "s" : ""}}</span>
  </header>
</template>

<style scoped>
.Header {
  background-color: #F0F8FF;
}
</style>