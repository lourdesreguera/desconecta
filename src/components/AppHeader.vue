<template>
  <header class="position-absolute top-0 start-0 w-100 z-2">
    <nav class="navbar navbar-expand-lg navbar-dark bg-transparent px-3 px-sm-3">
      <div class="container-xxl d-flex align-items-center">
        <a class="navbar-brand" href="#"><img src="../assets/logo-white-red.svg" alt="Logo (des)Conecta"
            width="400" /></a>
        <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#mainNav"
          aria-controls="mainNav" aria-expanded="false" aria-label="Toggle navigation">
          <span class="navbar-toggler-icon navbar-icon"></span>
        </button>
        <div class="collapse navbar-collapse justify-content-end" id="mainNav">
          <ul class="navbar-nav">
            <li class="nav-item">
              <a class="nav-link text-end text-white" href="#about">¿Qué es?</a>
            </li>
            <li class="nav-item">
              <a class="nav-link text-end text-white" href="#learning">¿Qué vas a aprender?</a>
            </li>
            <li class="nav-item">
              <a class="nav-link text-end text-white" href="#form">Solicita formación</a>
            </li>
          </ul>
        </div>
      </div>
    </nav>
  </header>
</template>

<style lang="scss" scoped>
img {
  @media screen and (max-width: 1100px) {
    width: 300px;
  }

  @media screen and (max-width: 500px) {
    width: 200px;
  }
}

.navbar-icon {
  background-image: url("data:image/svg+xml,<svg xmlns='http://www.w3.org/2000/svg' fill='%23ff302a' viewBox='0 0 30 30'><path stroke='rgba(255, 255, 255, 1)' stroke-linecap='round' stroke-miterlimit='10' stroke-width='2' d='M4 7h22M4 15h22M4 23h22'/></svg>");
}

#mainNav {
  @media screen and (max-width: 992px) {
    background-color: #e8e5e5ec;
    border-radius: 0.5rem;
    padding: 0.5rem 1rem 1rem 0.5rem;

    a {
      color: #000 !important;
      font-weight: 600;
    }
  }
}
</style>
