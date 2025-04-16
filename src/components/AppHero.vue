<template>
  <section class="hero-container position-relative d-flex align-items-end px-sm-3">
    <img src="../assets/hero.png" class="w-100 h-100 object-fit-cover position-absolute top-0 start-0"
      alt="Protege tu bienestar digital" />
    <div class="overlay position-absolute top-0 start-0 w-100"></div>

    <div
      class="container-xxl position-relative z-2 text-white pb-5 px-sm-3 d-flex flex-column align-items-center align-items-md-start gap-3">
      <h1 class="text-center text-md-start">Protege tu bienestar digital</h1>
      <div class="col-lg-6 text-center text-md-start">
        <p>(des)CONECTA ofrece formación gratuita para enseñar a jóvenes de 10 a 18 años a usar la tecnología de forma
          segura y saludable, y conocer los riesgos del uso excesivo de pantallas en su salud física y mental.</p>
      </div>
      <a class="btn btn-primary base-btn-border" href="#form">Solicita formación gratuita</a>
    </div>
  </section>
</template>

<style lang="scss" scoped>
@import '@/scss/mixins/_buttons.scss';

.hero-container {
  height: 34rem;

  .overlay {
    height: 50%;
    background: linear-gradient(rgba(0, 0, 0, 1), rgba(0, 0, 0, 0));
  }

  @media screen and (max-width: 400px) {
    height: 38rem;
  }
}

.base-btn-border {
  @include base-button(true, transparent);
}
</style>
