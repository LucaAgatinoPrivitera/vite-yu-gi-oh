<script>
import Header from './components/Header.vue'
import Main from './components/Main.vue'
import { store } from './store.js';
import axios from 'axios';

export default {
  components: {
    Header,
    Main
  },


  data() {
    return {
      appTitle: "Rick 'n' Morty",
      store, //Da chiedere, l'ho preso dal codice di Luca di oggi, ma lo devo mettere? dopo provo a toglierlo e vedo se si rompe qualcosa.
      searchString: "",
      searchType: "",
    }
  },


  methods: {
    getPersonaggi() {
      console.log("cerca: ", this.searchString); //il this serve perché è messo nel data, in fondo è vue

      axios.get("https://db.ygoprodeck.com/api/v7/cardinfo.php?num=10&offset=0" + this.searchString).then(risultato => {
        // console.log(risultato.data.results);
        this.store.carteAxios = risultato.data.data;
        // Mettendo il data mi becco tutto l'oggettone e quindi ha tutto dentro
        console.log(this.store.carteAxios)
      });
    },
    getName() {
      axios.get("https://db.ygoprodeck.com/api/v7/cardinfo.php?name=" + this.searchString).then(risultato => {
        this.store.carteAxios = risultato.data.data;
        // da chiedere, cosa fa nello specifico ma cerca il nome
      });
    },
    getTypes() {
      // endpoint dei tipi
      axios.get("https://db.ygoprodeck.com/api/v7/archetypes.php").then(risultato => {
        this.store.typeAxios = risultato.data;
        console.log(this.store.typeAxios[0])
      });
    },


    onChangeInput() {
      // endpoint dei tipi
      axios.get("https://db.ygoprodeck.com/api/v7/cardinfo.php?archetype=" + this.searchType).then(risultato => {
        this.store.carteAxios = risultato.data.data;
        console.log(this.store.typeAxios[0])
      });
    },

  },
  created() {
    this.getPersonaggi();
    this.getTypes()
  },
  mounted() {
  }
}

</script>

<template>
  <Header></Header>
  <select class="form-select bg-light w-75 m-auto" aria-label="Default select example" v-model="searchType"
    @change="onChangeInput()">
    <option selected disabled value>Open this select menu</option>
    <option v-for="archetipo in this.store.typeAxios" :key="archetipo.archetype_name" :value="archetipo.archetype_name">
      <!-- Prima senza key e value non funzionava -->
      {{ archetipo.archetype_name }}</option>
  </select>
  <Main></Main>
  <div class="w-75 m-auto px-3">
    <input type="text" v-model="searchString" placeholder="Cerca la carta">
    <button @click="getName()">Cerca</button>
  </div>

</template>

<style scoped>
.logo {
  height: 6em;
  padding: 1.5em;
  will-change: filter;
  transition: filter 300ms;
}

.logo:hover {
  filter: drop-shadow(0 0 2em #646cffaa);
}

.logo.vue:hover {
  filter: drop-shadow(0 0 2em #42b883aa);
}
</style>
