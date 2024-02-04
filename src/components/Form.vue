<script setup>
import { defineProps } from 'vue';
const {state, register} = defineProps(["state", "register"]);

function changeFilter({target}) {
  state.filter = target.value;
}

</script>

<template>
  <form class="Form container py-5 px-3" @submit.prevent>
    <div class="row">
      <input type="text" placeholder="Descreva aqui a tarefa..." class="col form-control" @change.prevent="register" required>
      <button type="submit" class="col-md-2 btn btn-primary my-3 my-md-0 mx-md-2">Cadastrar</button>
      <div class="col-md-2 p-0">
        <select class="form-select" @change="changeFilter">
          <option value="all">Todas</option>
          <option value="pending">Pendentes</option>
          <option value="completed">Finalizadas</option>
        </select>
      </div>
    </div>
  </form>
</template>