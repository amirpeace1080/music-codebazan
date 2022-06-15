<template>
  <v-app id="app">
    <Navbar />

    <v-container>
      <v-row class="mt-4">
        <v-col id="first" lg="3" cols="12">
          <RightMenu />
        </v-col>
        <v-col id="second" lg="6" cols="12">
          <v-main>
            <router-view />
          </v-main>
        </v-col>
        <v-col id="third" lg="3" cols="12">
          <LeftMenu />
        </v-col>
      </v-row>
    </v-container>
  </v-app>
</template>

<script>
import Navbar from "./components/Navbar.vue";
import RightMenu from "./components/RightMenu.vue";
import LeftMenu from "./components/LeftMenu.vue"

export default {
  components: { Navbar, RightMenu, LeftMenu },
  name: "App",
};
</script>

<style>
a {
  text-decoration: none;
}
a:hover {
  text-decoration: none;
}
#app {
   /* font-family: 'Caveat', cursive; */
  background-color: #eee;
  text-align: center;
  color: #2c3e50;
}

@media only screen and (max-width: 768px) {
  #first {
    order: 2;
  }
  #second {
    order: 1;
  }
  #third {
    order: 3;
  }
}
</style>
