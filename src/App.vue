<template>
  <v-app id="app">
    <v-main>
      <Navigation />
      <router-view />
    </v-main>
  </v-app>
</template>

<script>
import Navigation from "./components/Navigation";
export default {
  name: "App",
  components: {
    Navigation,
  },

  data: () => ({
    //
  }),
};
</script>
<style lang="scss">
@import "/src/sass/variables";
#app {
  background-color: map-get($colors, primary);
  font-family: "Raleway", sans-serif;
  letter-spacing: 0.1rem;
}

</style>
