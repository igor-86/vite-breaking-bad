<script>
export default {
    name: "AppHeader",
    data() {
        return {
            titleSite: "Breaking Bad Api",

        }
    },
    components: {

    },
}
</script>

<template>
    <header class="d-flex">
        <div class="img-logo">
            <img src="../assets/img/breaking-bad.png" alt="">
        </div>
        <h2>{{ titleSite }}</h2>
    </header>

</template>

<style lang="scss" scoped>
@use "../styles/general.scss" as*;

header {
    width: 100%;
    height: 80px;
    padding: 1rem 0;

    h2 {
        font-size: 2.5rem;
        font-weight: 700;
        color: white;
    }

    .img-logo {
        margin: 0 1rem;
        height: 100%;

        img {
            height: 100%;
        }
    }
}
</style>