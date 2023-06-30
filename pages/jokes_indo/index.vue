<template>
  <div class="container" style="margin-top: 100px">
    <h1 class="mb-4 border-bottom">Jokes Garing Bahasa Indonesia</h1>
    <Joke v-for="joke in jokesApi" :joke="joke" :key="joke.id" />
  </div>
</template>

<script>
import Joke from "../../components/ListJokesIndo";
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
      const res = await axios.get(
        "https://candaan-api.vercel.app/api/text",
        config
      );

      this.jokesApi = res.data.data;

      // console.log(res.data.data);
    } catch (error) {
      console.log(error);
    }
  },

  head() {
    return {
      title: "Jokes Garing Indonesia",
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
