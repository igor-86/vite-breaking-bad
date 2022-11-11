<script>
import { store } from '../store';
export default {
    name: "AppForm",
    data() {
        return {
            store,
            statusSelect: ["Breaking Bad", "Better Call Soul"],
        }
    }, components: {

    },
}
</script>

<template>
    <div class="container">
        <div class="form mt-1">
            <select name="" class="form-select" aria-label="Default select example" v-model="store.searchCategory">
                <option select value="">Select category</option>
                <option value="inner" v-for="(inner, index) in statusSelect" :key="index">{{ inner }}</option>
            </select>
            <button class="btn" @click="$emit('reSearch')">Search</button>
        </div>
    </div>

</template>

<style lang="scss" scoped>
.form {
    width: 50%;
    height: 100px;
    display: flex;
    align-items: center;



    .form-select {
        padding: 1rem;
        border-radius: 8px;
        border: none;
        font-size: 1.2rem;

    }

    .btn {
        background-color: white;
        border-radius: 8px;
        padding: .8rem 1.2rem;
        border: none;
        cursor: pointer;
        text-transform: uppercase;
        font-weight: 600;
        margin-left: 1rem;
    }
}
</style>