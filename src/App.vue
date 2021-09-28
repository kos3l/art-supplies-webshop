<template>
  <v-app id="app">
    <v-main>
      <v-container fluid class="secondary d-none d-md-block nav pa-0">
        <v-row class="height-fix">
          <v-col
            class="height-fix pa-0 pt-3 d-flex justify-center align-center"
          >
            <p class="ma-0">ASS</p>
          </v-col>
        </v-row>
        <v-row>
          <v-col class="nav-box d-flex justify-center"> PAINTING </v-col>
          <v-col class="nav-box d-flex justify-center"> DRAWING </v-col>
          <v-col class="nav-box d-flex justify-center"> BUNDLES </v-col>
        </v-row>
      </v-container>
      <router-view />
    </v-main>
  </v-app>
</template>

<script>
export default {
  name: "App",

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
  height: 3rem;
  font-weight: bold;
}
.nav p {
  color: map-get($colors, primary);
  font-style: italic;
}
.height-fix {
  height: 100%;
}
.nav-box {
  @include container_mixin(
    2px,
    map-get($colors, secondary),
    2rem,
    2rem,
    map-get($colors, secondary),
    map-get($colors, primary)
  );
}
.nav-box:first-child {
  margin-left: 2px;
  border-right: 0;
}
.nav-box:last-child {
  margin-right: 2px;
  border-left: 0;
}
</style>
