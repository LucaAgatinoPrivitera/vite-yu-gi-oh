<script>
import { ref } from 'vue'
import Main_ContainerCards from '../components/Main_ContainerCards.vue'
import { store } from '../store.js';
import axios from 'axios'


export default {
  components: {
    Main_ContainerCards
  },
  data() {
    return {
      store
    }
  }
}
</script>

<template>
  <div class="d-flex px-4 py-4 w-100">
    <div class="w-75 m-auto">
      <div class="dropdown">
        <!--<button class="btn btn-light dropdown-toggle" type="button" data-bs-toggle="dropdown" aria-expanded="false">
          Seleziona type
        </button>
         <ul class="dropdown-menu">
          <li v-for="archetipo in this.store.typeAxios"><a class="dropdown-item"
              href="#">{{ archetipo.archetype_name }}</a></li>
        </ul> -->
      </div>
    </div>
  </div>
  <Main_ContainerCards></Main_ContainerCards>
</template>

<style scoped>
div {
  background-color: orange;
}

button {
  padding-inline-end: 2rem;
}
</style>
