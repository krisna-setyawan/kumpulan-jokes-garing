<template>
  <div class="container" style="margin-top: 100px">
    <h1 class="mb-4 border-bottom">Kumpulan Meme</h1>

    <div class="row">
      <Meme
        v-for="(meme, index) in memesApi"
        :memeUrl="meme.url"
        :key="index"
      />
    </div>
  </div>
</template>

<script>
import Meme from "../../components/ListMeme";
import axios from "axios";

export default {
  components: {
    Meme,
  },

  data() {
    return {
      memesApi: [],
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
        "https://candaan-api.vercel.app/api/image",
        config
      );

      this.memesApi = res.data.data;
    } catch (error) {
      console.log(error);
    }
  },

  head() {
    return {
      title: "Jokes Garing Inggris",
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
