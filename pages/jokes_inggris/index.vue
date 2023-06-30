<template>
  <div class="container" style="margin-top: 100px">
    <h1 class="mb-4 border-bottom">Jokes Garing Bahasa Inggris</h1>
    <Joke
      v-for="joke in jokesApi"
      :joke="joke.joke"
      :key="joke.id"
      :id="joke.id"
    />
  </div>
</template>

<script>
import Joke from "../../components/ListJokesInggris";
import axios from "axios";

export default {
  components: {
    Joke,
  },

  data() {
    return {
      jokesApi: [],
    };
  },

  async created() {
    const config = {
      headers: {
        Accept: "application/json",
      },
    };

    try {
      const res = await axios.get("https://icanhazdadjoke.com/search", config);

      this.jokesApi = res.data.results;
    } catch (error) {
      console.log(error);
    }
  },

  head() {
    return {
      title: "Jokes Garing",
      meta: [
        {
          hid: "deskripsi",
          name: "deskripsi",
          content: "Kumpulan jokes jokes garing",
        },
      ],
    };
  },
};
</script>
