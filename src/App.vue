

<script>
//Import
import axios from "axios";
import AppHeader from './components/AppHeader.vue';
import AppForm from './components/AppForm.vue';
import AppBoxcard from './components/AppBoxcard.vue';

import { store } from "./store";

export default {
  name: "AppVue",
  data() {
    return {
      store
    }
  },
  components: {
    AppHeader,
    AppForm,
    AppBoxcard,
  },
  created() {
    this.getCharacters();
  },
  methods: {
    getCharacters() {
      let apiUrl = "https://www.breakingbadapi.com/api/characters";

      const urlCategory = {};
      if (this.store.searchCategory) {
        urlCategory.category = this.store.searchCategory;
      }

      axios.get(apiUrl, { params: urlCategory }).then((resp) => {
        this.store.characters = resp.data;
      })
    }



    /* getCharacters() {
      axios.get("https://www.breakingbadapi.com/api/characters").then((resp) => {
        
        this.store.characters = resp.data;
        console.log(this.store.characters);
      })
    } */
  },


}
</script>

<template>
  <AppHeader />
  <AppForm @reSearch="getCharacters" />
  <AppBoxcard />
</template>

<style lang="scss">
@use "./styles/general.scss" as*;
@use "./styles/partials/variables.scss" as*;
</style>