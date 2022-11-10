<script>
//Import
import { store } from "../store";
import AppCard from './AppCard.vue';
export default {
    name: "AppBoxcard",
    data() {
        return {
            store
        }
    },
    components: {
        AppCard,
    },
}
</script>

<template>
    <main>
        <div class="container">
            <div class="slide">
                <div class="row row-wrap">
                    <div class="cards" v-for="inner in store.characters" :key="inner.char_id">
                        <AppCard :character="inner" />
                    </div>
                </div>
            </div>
        </div>
    </main>
</template>

<style lang="scss" scoped>
@use "../styles/general.scss";
@use "../styles/partials/variables.scss";

.slide {
    width: 100%;
    background-color: white;
    padding: 2rem;

    .cards {
        width: calc(100% / 5 - 1rem);
        padding: 1.5rem;
        background-color: #0d0d2b;

    }
}
</style>