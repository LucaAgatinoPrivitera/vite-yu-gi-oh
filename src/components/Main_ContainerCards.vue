<script>
import { ref } from 'vue';
import { store } from '../store.js';
import axios from 'axios'

export default {
    name: "CardsList",
    data() {
        return {
            store
        }
    },
    methods: {

    },
    mounted() {

    }


}
</script>

<template>
    <div id="primodiv" class="d-flex px-4 py-4 w-100">
        <div class="bg-transparent text-light w-75 m-auto p-0">
            <div class="bg-light p-4">
                <h3 class="p-3 m-0 bg-dark">Found 39 cards</h3>
                <!-- <pre>{{store.carte}}</pre> -->

                <!--  
                <div class="d-flex flex-wrap justify-content-between m-0 p-0 bg-light">
                    <div class="cardSingola mb-3" v-for="cardSingola, i in store.carte">
                        <img :src="cardSingola.card_images[0].image_url">
                        <h6 class="text-center">{{ cardSingola.name }}</h6>
                        <p class="text-center text-dark">{{ cardSingola.archetype }}</p>
                    </div>
                </div>
                -->
                <h3 class="text-light bg-primary p-3 mb-0 mt-4">Part 2</h3>
                <h3 class="text-light bg-dark p-3 mb-0">Found 39 cards</h3>
                <div class="d-flex flex-wrap justify-content-between m-0 p-0 bg-light">
                    <div class="cardSingola mb-3" v-for="cardSingola, i in store.carte">
                        <img :src="cardSingola.card_images[0].image_url">
                        <h6 class="text-center">{{ cardSingola.name }}</h6>
                        <p class="text-center text-dark">{{ cardSingola.archetype }}</p>
                    </div>
                </div>
            </div>
        </div>
    </div>

</template>

<style scoped>
#primodiv {
    background-color: orange;
}

div {
    background-color: orange;
}

button {
    padding-inline-end: 2rem;
}

.cardSingola {
    width: 200px;
}

img {
    width: 200px;
}
</style>
