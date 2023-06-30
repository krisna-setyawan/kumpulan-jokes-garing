<template>
  <div style="margin-top: 100px">
    <div class="px-4 py-5 my-5 text-center">
      <img
        class="d-block mx-auto mb-4 rounded shadow-lg"
        src="https://img.freepik.com/premium-photo/man-wearing-glasses-is-laughing-while-looking-his-phone_909234-852.jpg?w=1380"
        alt=""
        width="30%"
      />
      <h1 class="display-5 fw-bold text-body-emphasis">
        Kumpulan Jokes Garing
      </h1>
      <div class="col-lg-6 mx-auto">
        <p class="lead mb-4">
          Lorem ipsum dolor sit amet consectetur, adipisicing elit. Cum adipisci
          eos illum repellat iusto minus hic velit veritatis ab placeat modi
          facere earum praesentium vel minima, ratione sint quaerat asperiores.
        </p>
        <div class="d-grid gap-2 d-sm-flex justify-content-sm-center">
          <nuxt-link
            to="/jokes_indo"
            class="btn btn-outline-secondary btn-lg px-4 gap-3"
          >
            Lihat Jokes Indonesia
          </nuxt-link>
          <nuxt-link
            to="/jokes_inggris"
            class="btn btn-outline-danger btn-lg px-4"
          >
            Lihat Jokes Inggris
          </nuxt-link>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  head() {
    return {
      title: "Kumpulan Jokes Garing",
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

<style></style>
