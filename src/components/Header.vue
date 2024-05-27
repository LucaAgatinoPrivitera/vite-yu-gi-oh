<script setup>
import { ref } from 'vue'

defineProps({
  msg: String,
})

const count = ref(0)
</script>

<template>
  <div class="d-flex mx-4 my-2">
    <img src="" alt="">
    <h1>Yu-Gi-Oh-Api</h1>
  </div>
</template>

<style scoped>
.read-the-docs {
  color: #888;
}
</style>
