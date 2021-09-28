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

.nav {
  height: 2.5rem;
  font-weight: bold;
}
.nav p {
  color: map-get($colors, primary);
  font-style: italic;
  font-size: 0.9rem;
}
.height-fix {
  height: 100%;
}
.nav-box {
  @include container_mixin(
    3px,
    map-get($colors, secondary),
    0.875rem,
    0,
    map-get($colors, secondary),
    map-get($colors, primary)
  );
  font-size: 1.1rem;
}
</style>
