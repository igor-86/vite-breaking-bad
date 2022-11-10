<script>
export default {
    name: "AppCard",
    props: {
        character: Object
    },
    data() {
        return {
            title: "Breaking Bad"
        }
    },
    components: {

    },
}
</script>

<template>
    <div class="img-card">
        <img :src="character.img" alt="">
    </div>
    <h3>{{ character.name }}</h3>
    <h4>{{ title }}</h4>
    <h4>{{ character.status }}</h4>

</template>

<style lang="scss" scoped>
.img-card {
    width: 100%;
    height: 300px;

    img {
        object-fit: cover;
        object-position: center;
        height: 100%;
    }
}

h3 {
    color: white;
    text-transform: uppercase;
    font-weight: 700;
    font-size: 1.4rem;
    text-align: center;
    margin-bottom: 2rem;
    margin-top: 1rem;

}

h4 {
    color: #565656;
    text-align: center;
    font-size: 1.4rem;
    margin-bottom: .8rem;
}
</style>