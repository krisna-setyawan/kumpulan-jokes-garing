<template>
  <div class="col-md-4 mb-4">
    <img class="rounded shadow" :src="memeUrl" alt="" width="100%" />
  </div>
</template>

<script>
export default {
  name: "Meme",
  props: ["memeUrl"],
};
</script>
