<template>
  <div>
    <h1>Random bible verse</h1>
    <input type="button" @click="fetchRandomVerse" value="random bible verse" />
    <p v-if="result">{{ result }}</p>
  </div>
</template>

<script setup>
import axios from 'axios'
import { ref } from 'vue'

const result = ref(null)

function fetchRandomVerse() {
  axios
    .get(`https://bible-api.com/data/web/random`)
    .then((response) => {
      result.value = response.data
    })
    .catch((error) => {
      console.error('API get failed', error)
    })
}
</script>

<style lang="scss" scoped></style>
