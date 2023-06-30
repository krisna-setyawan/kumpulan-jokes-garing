<template>
  <header class="py-3 mb-3 px-4 shadow-lg fixed-top">
    <div
      class="d-flex flex-wrap align-items-center justify-content-center justify-content-lg-start container"
    >
      <p
        class="d-flex align-items-center mb-0 mb-md-0 me-md-auto link-body-emphasis text-decoration-none"
      >
        <span class="fs-4 fw-bold text-warning ms-2"
          >Kumpulan Jokes Garing</span
        >
      </p>

      <ul class="nav nav-pills">
        <li class="nav-item">
          <nuxt-link to="/" class="nav-link text-light fs-5 ms-3"
            >Home</nuxt-link
          >
        </li>
        <li class="nav-item">
          <nuxt-link to="/jokes_indo" class="nav-link text-light fs-5 ms-3"
            >Jokes Indonesia</nuxt-link
          >
        </li>
        <li class="nav-item">
          <nuxt-link to="/jokes_inggris" class="nav-link text-light fs-5 ms-3"
            >Jokes Inggris</nuxt-link
          >
        </li>
        <li class="nav-item">
          <nuxt-link to="/about" class="nav-link text-light fs-5 ms-3"
            >About</nuxt-link
          >
        </li>
      </ul>
    </div>
  </header>
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
  font-weight: bold;
}
</style>
