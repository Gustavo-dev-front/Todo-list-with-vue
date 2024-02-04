<script setup>
</script>

<template>
  <ul class="List list-group container px-3 p-0">
    <li class="list-group-item d-flex align-items-center gap-2">
      <input type="checkbox" id="teste1">
      <label for="teste1">Tarefa xpto</label>
    </li>
    <li class="list-group-item d-flex align-items-center gap-2 done">
      <input type="checkbox" id="teste2">
      <label for="teste2">Tarefa xpto</label>
    </li>
  </ul>
</template>

<style scoped>
.done {
  text-decoration: line-through;
}
</style>