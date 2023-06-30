<template>
  <div class="container" style="margin-top: 100px">
    <div class="mb-3">
      <nuxt-link to="/jokes_inggris">
        <button class="btn btn-sm btn-danger">
          <b>&#11164;</b> &nbsp; Kembali ke List Jokes
        </button>
      </nuxt-link>
    </div>

    <h2>{{ jokeApi }}</h2>
    <hr />
    <small>Joke ID : {{ $route.params.id }}</small>
  </div>
</template>

<script>
import axios from "axios";

export default {
  data() {
    return {
      jokeApi: [],
    };
  },

  async created() {
    const config = {
      headers: {
        Accept: "application/json",
      },
    };

    try {
      const res = await axios.get(
        `https://icanhazdadjoke.com/j/${this.$route.params.id}`,
        config
      );

      this.jokeApi = res.data.joke;
    } catch (error) {
      console.log(error);
    }
  },
};
</script>
