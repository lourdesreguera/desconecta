<script setup>
defineProps({ submittedList: Array });
</script>

<template>
  <h3 class="text-center mb-4">Datos registrados</h3>
  <div class="table-responsive">
    <table class="table table-bordered">
      <thead>
        <tr>
          <th>#</th>
          <th>Nombre</th>
          <th>Apellidos</th>
          <th>Email</th>
          <th>Teléfono</th>
        </tr>
      </thead>
      <tbody>
        <tr v-for="(submittedData, index) in submittedList" :key="index">
          <td>{{ index + 1 }}</td>
          <td>{{ submittedData.name }}</td>
          <td>{{ submittedData.surname }}</td>
          <td>{{ submittedData.email }}</td>
          <td>{{ submittedData.telephone }}</td>
        </tr>
      </tbody>
    </table>
  </div>
</template>
