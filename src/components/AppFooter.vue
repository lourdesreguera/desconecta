<script setup>
const shortcutsItems = [
  { text: 'Qué es', href: '#about' },
  { text: 'Qué vas a aprender', href: '#learning' },
  { text: 'Solicita formación gratuita', href: '#form' }
];

const bottomNavItems = [
  { text: 'Política de privacidad', href: '#' },
  { text: 'Términos y condiciones', href: '#' },
  { text: 'Política de cookies', href: '#' },
  { text: 'Accesibilidad web', href: '#' },
  { text: 'Fundación Cibervoluntario 2024', href: '#' }
];
</script>

<template>
  <footer class="d-flex align-items-end position-relative">
    <div class="container-xxl px-sm-4">
      <img src="../assets/logo-white.svg" alt="Desconecta logo" width="450" />
      <div class="row g-4">
        <div class="col-sm-6 col-lg-4">
          <h4 class="text-white fw-bold">Accesos rápidos</h4>
          <hr class="border-white w-50">
          <nav>
            <ul class="list-unstyled d-flex flex-column gap-2">
              <li v-for="(item, i) in shortcutsItems" :key="i"><a class="list-item" :href="item.href">{{ item.text
              }}</a></li>
            </ul>
          </nav>
        </div>

        <div class="col-sm-6 col-lg-4">
          <h4 class="text-white fw-bold">Contáctanos</h4>
          <hr class="border-white w-50">
          <ul class="list-unstyled d-flex flex-column gap-2">
            <li><i class="bi bi-telephone-fill"></i><a class="list-item" href="tel:+34674727623" target="_blank"> +34
                674 72 76 23</a>
            </li>
            <li class="flex"><i class="bi bi-envelope-fill me-2"></i><a class="list-item"
                href="mailto:fundacion@cibervoluntarios.org" target="_blank">
                fundacion@cibervoluntarios.org</a></li>
            <li><i class="bi bi-globe me-2"></i><a class="list-item" href="https://cibervoluntarios.org"
                target="_blank">
                cibervoluntarios.org</a></li>
          </ul>
        </div>

        <div class="col-md-12 col-lg-4">
          <h4 class="text-white fw-bold">Conecta con nosotros</h4>
          <hr class="border-white w-50">
          <div class="d-flex gap-3">
            <i class="bi bi-instagram"></i>
            <i class="bi bi-facebook"></i>
            <i class="bi bi-twitter-x"></i>
            <i class="bi bi-youtube"></i>
            <i class="bi bi-linkedin"></i>
            <i class="bi bi-tiktok"></i>
            <i class="bi bi-whatsapp"></i>
          </div>
        </div>

        <hr class="border-white">

        <div class="row p-0 px-sm-4">
          <div class="col-12 d-flex justify-content-center justify-content-md-start g-1 g-lg-2">
            <nav>
              <ul class="list-unstyled d-flex flex-column align-items-center w-100 flex-md-row gap-1 gap-md-2 gap-xl-5">
                <li v-for="(item, i) in bottomNavItems" :key="i"><a :href="item.href" class="bottom-nav-item">{{
                  item.text }}</a>
                </li>
              </ul>
            </nav>
          </div>
        </div>
      </div>
    </div>
  </footer>
</template>

<style lang="scss" scoped>
@import '@/scss/_variables.scss';

footer {
  background-image: url('../assets/red-bg.png');
  background-repeat: no-repeat;
  background-size: cover;
  background-position: top;
  height: 35rem;

  @media screen and (max-width: 991px) {
    height: 45rem;
  }

  @media screen and (max-width: 768px) {
    background-image: none;
    background-color: $primary;
    height: fit-content;
  }
}

img {
  @media screen and (max-width: 768px) {
    width: 80vw;
  }

  @media screen and (max-width: 600px) {
    width: 90vw;
  }
}


h4 {
  font-size: 1.125rem;
}

.list-item,
.bottom-nav-item {
  color: #fff;
  text-decoration: none;
  font-size: 0.9375rem;

  &:hover {
    color: #000;
  }
}

i {
  color: #fff;
}

.bottom-nav-item {
  font-size: 1rem;
}
</style>
