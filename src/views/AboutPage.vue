<template>
  <div>
    <h1>Random bible verse</h1>
    <!-- knapp som hämtar från fetch funktionen -->
    <input type="button" @click="fetchRandomVerse" value="random bible verse" />
    <!-- Kompunänten ränderas ifall vi har fått ett resultat -->
    <div class="verses" v-if="result !== null">
      <RandomVerseComponent
        :book="result.random_verse.book"
        :chapter="result.random_verse.chapter"
        :verse="result.random_verse.verse"
        :text="result.random_verse.text"
      />
    </div>
  </div>
</template>

<script setup>
import axios from 'axios'
import { ref } from 'vue'
import RandomVerseComponent from '../components/RandomVerseComponent.vue'

const result = ref(null)

//function som fetchar api från bibelverses
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
