<template>
  <v-app>
    <Navbar />

    <v-main>
      <router-view/>
    </v-main>
  </v-app>
</template>

<script>
import Navbar from './components/Navbar.vue';

export default {
  components: { Navbar },
  name: 'App',

  data: () => ({
    //
  }),
};
</script>

<style>
a {
  text-decoration: none;
}
a:hover {
  text-decoration: none;
}
</style>
