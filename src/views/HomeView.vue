<template>
  <div>
    <v-btn block color="primary" @click="search">Search</v-btn>
    {{ showResult }}
  </div>
</template>

<script>
import axios from "axios";
export default {
  name: "Home",
  data() {
    return {
      showResult: [],
    };
  },
  methods: {
    async search() {
      // this.showSearch = true;
      // await axios
      //   .get(`http://api.codebazan.ir/music/?type=search&query=hamed&page=1`)
      //   .then((res) => {
      //     this.showResult = res.data
      //   });

      await axios
        .get("http://api.codebazan.ir/music/?type=search&query=hamed&page=1")
        .then((res) => {
          console.log("Everything is awesome.", res);
        })
        .catch((error) => {
          console.warn("Not good man :(", error);
          this.showResult = error
        });
    },
  },
};
</script>

<style scoped>
</style>