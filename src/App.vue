<script>
import axios from "axios";
import AppHeader from "./components/AppHeader.vue";
import AppMain from "./components/AppMain.vue";
import { store } from "./store";

export default {
  components: {
    AppHeader,
    AppMain,
  },
  data() {
    return {
      store
    }
  },
  created() {
    axios.get("https://rickandmortyapi.com/api/character").then((resp) => {
      this.store.characters = resp.data.results;
      console.log(this.store.characters);
    })
  }
}
</script>

<template>
  <AppHeader />
  <main>
    <AppMain />

  </main>
</template>

<style lang="scss">
@use "./styles/general.scss" as *;
</style>