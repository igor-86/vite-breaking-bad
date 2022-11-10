

<script>
//Import
import AppHeader from './components/AppHeader.vue';
import AppForm from './components/AppForm.vue';
import AppBoxcard from './components/AppBoxcard.vue';

export default {
  name: "AppVue",
  data() {
    return {

    }
  },
  components: {
    AppHeader,
    AppForm,
    AppBoxcard,
  },
}
</script>

<template>
  <AppHeader />
  <AppForm />
  <AppBoxcard />
</template>

<style lang="scss">
@use "./styles/general.scss" as*;
</style>