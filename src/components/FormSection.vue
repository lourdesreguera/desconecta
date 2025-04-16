<script setup>
import { ref } from 'vue';
import TrainingForm from './TrainingForm.vue';

const name = ref('');
const surname = ref('');
const email = ref('');
const telephone = ref('');
const submittedList = ref([])

const handleSubmit = (e) => {
  e.preventDefault();

  if (name.value && surname.value && email.value && telephone.value) {
    submittedList.value.push({
      name: name.value,
      surname: surname.value,
      email: email.value,
      telephone: telephone.value
    });
  }

  name.value = '';
  surname.value = '';
  email.value = '';
  telephone.value = '';
};

</script>

<template>
  <section class="mx-auto px-3 px-sm-4 position-relative" id="form">
    <h2 class="text-center text-primary mb-5">Solicita formación gratuita</h2>
    <form class="row g-4">
      <div class="col-md-5">
        <input v-model="name" type="text" class="form-control" placeholder="*Nombre" required>
      </div>
      <div class="col-md-7">
        <input v-model="surname" type="text" class="form-control" placeholder="*Apellidos" required>
      </div>
      <div class="col-md-7">
        <input v-model="email" type="email" class="form-control" placeholder="*Email" required>
      </div>
      <div class="col-md-5">
        <input v-model="telephone" type="number" class="form-control" placeholder="*Teléfono" required>
      </div>
      <div class="col-12">
        <button type="submit" class="btn btn-primary base-btn mt-3" @click="handleSubmit">Solicita</button>
      </div>
    </form>

    <div v-if="submittedList.length" class="mt-5">
      <TrainingForm :submittedList="submittedList" />
    </div>
  </section>
</template>

<style lang="scss" scoped>
@import '@/scss/mixins/_buttons.scss';

section {
  bottom: calc(8rem - 3rem);
  max-width: 70rem;
}

input {
  border-radius: 3.125rem !important;
  border-color: #000 !important;
  padding: 0.9375rem 1.875rem !important;
}

input::placeholder {
  color: #9E9E9E !important;
}

.base-btn {
  @include base-button();
  width: 12.5rem;
}
</style>
