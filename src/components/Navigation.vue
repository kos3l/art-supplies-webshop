<template>
  <v-container fluid class="secondary d-none d-md-block nav pa-0">
    <v-row class="height-fix">
      <v-col class="height-fix pa-0 pt-3 d-flex justify-center align-center">
        <p class="ma-0">ART SUPPLY STORE</p>
      </v-col>
    </v-row>
    <v-row>
      <v-col class="pa-0">
        <div
          class="nav-box d-flex justify-center"
          style="border-right:0;"
          id="home"
        >
          PAINTING
        </div>
      </v-col>
      <v-col class="pa-0">
        <div class="nav-box d-flex justify-center" id="drawing">
          DRAWING
        </div>
      </v-col>
      <v-col class="pa-0">
        <div
          class="nav-box d-flex justify-center"
          style="border-left:0;"
          id="bundles"
        >
          BUNDLES
        </div>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
export default {
  name: "Navigation",

  data() {
    return {
      currentPage: this.$router.currentRoute.path,
      home: document.getElementById("home"),
    };
  },
  mounted: {
    currentPageStyle: function() {
      if (this.currentPage == "/painting") {
        return this.home.classList.add("current");
      }
    },
  },
};
</script>

<style lang="scss">
@import "/src/sass/variables";

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
.nav-box:hover {
  @include container_mixin(
    3px,
    map-get($colors, secondary),
    0.875rem,
    0,
    map-get($colors, primary),
    map-get($colors, secondary)
  );
}
.current {
  background-color: map-get($colors, secondary);
}
</style>
