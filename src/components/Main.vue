<script>
import { ref } from 'vue'
import Main_ContainerCards from '../components/Main_ContainerCards.vue'


export default {
  components: {
    Main_ContainerCards
  },
}
</script>

<template>
  <div class="d-flex px-4 py-4 w-100">
    <div class="w-75 m-auto">
      <button class="btn btn-outline-secondary dropdown-toggle bg-white" type="button" data-toggle="dropdown"
        aria-haspopup="true" aria-expanded="false">Alien</button>
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
