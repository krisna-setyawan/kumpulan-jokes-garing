<template>
  <nuxt-link class="joke-link" :to="'jokes_inggris/' + id">
    <div class="joke">
      <p class="mb-0">{{ joke }}</p>
    </div>
  </nuxt-link>
</template>

<script>
export default {
  name: "Joke",
  props: ["joke", "id"],
};
</script>

<style>
.joke {
  padding: 1rem;
  border: 1px solid #ccc;
  margin: 1rem 0;
}

.joke-link {
  text-decoration: none;
  color: #333;
}

.joke-link:hover {
  color: rgb(160, 58, 54);
  font-weight: bold;
}
</style>
