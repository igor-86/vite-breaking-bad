<script>
//Import
import AppCard from './AppCard.vue';
export default {
    name: "AppBoxcard",
    data() {
        return {

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
                    <div class="cards">
                        <AppCard />
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