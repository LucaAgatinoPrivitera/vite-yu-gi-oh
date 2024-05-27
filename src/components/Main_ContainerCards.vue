<script>
import { ref } from 'vue';
import store from '../store.js';

export default {
    name : "CardsList",
    data() {
        return {
            store
        }
    }
}
</script>

<template>
    <div class="d-flex px-4 py-4 w-100 bg-white">
        <div class="bg-dark text-light w-75 m-auto p-3">
            <h3>Found 39 cards</h3>
            <div>
                <div class="cardSingola" v-for="cardSingola in carte"></div>
            </div>
        </div>
    </div>

</template>

<style scoped>
div {
    background-color: orange;
}

button {
    padding-inline-end: 2rem;
}
</style>
