<template>
  <div>
    <input v-model="inputVerse" placeholder="search for a bibleverse" />
    <input type="button" @click="fetchBibleVerse" value="search" />
    <p v-if="result">{{ result }}</p>
  </div>
</template>

<script setup>
import { ref } from 'vue'
import axios from 'axios'

const inputVerse = ref('')
const result = ref(null)

function fetchBibleVerse() {
  axios
    .get(`https://bible-api.com/${inputVerse.value}`)
    .then((response) => {
      result.value = response.data
    })
    .catch((error) => {
      console.error('API get failed', error)
    })
}
</script>

<style lang="scss" scoped></style>
