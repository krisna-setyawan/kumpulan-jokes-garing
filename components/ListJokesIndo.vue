<template>
  <div class="joke">
    <p class="mb-0">{{ joke }}</p>
  </div>
</template>

<script>
export default {
  name: "Joke",
  props: ["joke"],
};
</script>

<style>
.joke {
  padding: 1rem;
  border: 1px solid #ccc;
  margin: 1rem 0;
}

.joke:hover {
  color: rgb(160, 58, 54);
  font-weight: bold;
}
</style>
