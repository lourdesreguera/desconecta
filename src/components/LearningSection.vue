<script setup>
import img1 from '../assets/learning-1.png'
import img2 from '../assets/learning-2.png'
import img3 from '../assets/learning-3.png'
import LearningCard from './LearningCard.vue'

const data = [
  {
    html: 'Identificar los posibles <strong>síntomas de un uso excesivo de dispositivos,</strong> como la dificultad para conciliar el sueño, la sensación de ansiedad, la falta de concentración o los cambios de estado de ánimo, entre otros.',
    image: img1,
    alt: "Persona experimentando síntomas de uso excesivo de pantallas"
  },
  {
    html: 'Reconocer las <strong>posibles adicciones</strong> que pueden surgir de este uso excesivo de las pantallas, como la <strong>nomofobia, el vamping, el phubbing o el síndrome FOMO.</strong> Esto permitirá a las personas jóvenes reflexionar sobre sus propios hábitos digitales.',
    image: img2,
    alt: "Personas representando diferentes adicciones digitales como nomofobia o FOMO"
  },
  {
    html: 'Conocer las <strong>herramientas de desconexión digital en sus dispositivos</strong> para mejorar su tiempo de conexióny establecer límites saludables, promoviendo así un equilibrio más positivo entre su vida digital y su bienestar personal.',
    image: img3,
    alt: "Personas representando herramientas para desconexión digital y bienestar personal"
  },
]
</script>

<template>
  <section id="learning" class="position-relative">
    <div class="main-container container d-flex flex-column align-items-center gap-4">
      <h2 class="text-primary text-center">¿Qué vas a aprender?</h2>
      <p class="description-text text-center">En (des)CONECTA - Conéctate contra la tecnoadicción, organizamos <span
          class="fw-bold">cursos gratuitos para
          enseñar a jóvenes de 10
          a
          18 años sobre el uso consciente, seguro y responsable de la tecnología,</span> ayudándoles a comprender cómo
        el uso
        excesivo de pantallas puede afectar a su salud física y mental. Las personas participantes aprenderán a:
      </p>
      <div class="container card-container">
        <div class="row row-cols-1 row-cols-lg-2 row-cols-xl-3 g-3">
          <div class="col d-flex justify-content-center"
            :class="{ 'mx-auto': data.length % 2 !== 0 && index === data.length - 1 }" v-for="(item, index) in data"
            :key="index">
            <LearningCard :item="item" :index="index" />
          </div>
        </div>
      </div>
      <a class="base-btn btn btn-primary mt-3" href="#form">Solicita formación gratuita</a>
    </div>
  </section>
</template>

<style lang="scss" scoped>
@import '@/scss/_variables.scss';
@import '@/scss/mixins/_buttons.scss';

section {
  bottom: 8rem;
}

.main-container {
  background-color: $grey;
  padding: 4rem;
  border-radius: 3.125rem;

  @media screen and (max-width: 1024px) {
    padding: 4rem 2rem 4rem 2rem;
  }

  @media screen and (max-width: 425px) {
    padding: 4rem 1rem 4rem 1rem;
  }
}

.card-container {
  max-width: 70rem;
}

.description-text {
  max-width: 60rem;
}

.base-btn {
  @include base-button();
}
</style>
