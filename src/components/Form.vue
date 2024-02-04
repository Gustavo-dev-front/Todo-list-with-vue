<script setup>
</script>

<template>
  <form class="Form container py-5 px-3">
    <div class="row">
      <input type="text" placeholder="Descreva aqui a tarefa..." class="col form-control" required>
      <button class="col-md-2 btn btn-primary my-3 my-md-0 mx-md-2">Cadastrar</button>
      <div class="col-md-2 p-0">
        <select class="form-select">
          <option value="todas">Todas</option>
          <option value="pendentes">Pendentes</option>
          <option value="finalizadas">Finalizadas</option>
        </select>
      </div>
    </div>
  </form>
</template>