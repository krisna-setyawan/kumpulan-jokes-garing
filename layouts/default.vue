<template>
  <div>
    <AppHeader />
    <div class="container-fluid">
      <nuxt />
    </div>
    <AppFooter />
  </div>
</template>

<script>
import AppHeader from "../components/AppHeader";
import AppFooter from "../components/AppFooter";

export default {
  components: {
    AppHeader,
    AppFooter,
  },
};
</script>
