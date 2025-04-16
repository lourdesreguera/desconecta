<template>
  <section class="py-5 px-3 px-sm-3" id="about">
    <div class="main-container d-flex flex-column align-items-center gap-5 mx-auto">
      <h2 class="text-primary">¿Qué es?</h2>
      <p class="text-center mb-0"><span class="fw-bold">Cursos gratuitos para jóvenes de entre 10 y 18 años para
          enseñarles a
          usar la tecnología de
          manera saludable,
          positiva y responsable.</span> Además, aprenderán sobre los riesgos de pasar demasiado tiempo frente a las
        pantallas y
        cómo esto puede afectar tanto a su salud física como mental. Cualquier centro educativo o entidad que trabaje en
        la educación de jóvenes puede solicitarlos.
      </p>
      <a class="btn btn-primary base-btn" href="#form">Solicita formación gratuita</a>
      <img src="../assets/video.png" alt="Desconecta video" width="400" />
    </div>
  </section>
</template>

<style lang="scss" scoped>
@import '@/scss/mixins/_buttons.scss';

section {
  background-image: url('../assets/light-red-bg.png');
  background-repeat: no-repeat;
  background-size: 100% 60%;
  background-position: center bottom;
}

.main-container {
  max-width: 70rem;
}

.base-btn {
  @include base-button();
}

img {
  width: 100%;
  margin-bottom: 13rem;
}
</style>
