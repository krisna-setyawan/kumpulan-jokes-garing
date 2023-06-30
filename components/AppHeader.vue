<template>
  <nav
    class="navbar navbar-expand-lg navbar-dark bg-dark fixed-top py-3 shadow-lg"
  >
    <div class="container">
      <nuxt-link class="navbar-brand fs-4 fw-bold text-warning ms-2" to="/"
        >Kumpulan Jokes Garing
      </nuxt-link>
      <button
        class="navbar-toggler"
        type="button"
        data-bs-toggle="collapse"
        data-bs-target="#navbarText"
        aria-controls="navbarText"
        aria-expanded="false"
        aria-label="Toggle navigation"
      >
        <span class="navbar-toggler-icon"></span>
      </button>
      <div class="collapse navbar-collapse" id="navbarText">
        <span class="navbar-text me-auto"> </span>
        <ul class="navbar-nav mb-2 mb-lg-0">
          <li class="nav-item">
            <nuxt-link to="/" class="nav-link text-light fs-5 ms-3"
              >Home
            </nuxt-link>
          </li>
          <li class="nav-item">
            <nuxt-link to="/jokes_indo" class="nav-link text-light fs-5 ms-3"
              >Jokes Indonesia
            </nuxt-link>
          </li>
          <li class="nav-item">
            <nuxt-link to="/jokes_inggris" class="nav-link text-light fs-5 ms-3"
              >Jokes Inggris
            </nuxt-link>
          </li>
          <li class="nav-item">
            <nuxt-link to="/meme" class="nav-link text-light fs-5 ms-3"
              >Meme
            </nuxt-link>
          </li>
          <li class="nav-item">
            <nuxt-link to="/about" class="nav-link text-light fs-5 ms-3"
              >About
            </nuxt-link>
          </li>
        </ul>
      </div>
    </div>
  </nav>
</template>

<script>
export default {
  name: "AppHeader",
};
</script>

<style>
header {
  background-color: #767f8b;
}
.nuxt-link-exact-active {
  font-weight: bolder;
}
</style>
