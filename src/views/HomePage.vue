<template>
  <div>
    <h1>search for a bibleverse</h1>
    <!-- Inputfält -->
    <input v-model="inputVerse" placeholder="Exemple Romans 8:31" />
    <!-- knapp som hämtar från fetch funktionen -->
    <input type="button" @click="fetchBibleVerse" value="search" />
    <!-- Kompunänten renderas ifall vi har fått ett resultat -->
    <div class="verses" v-if="result !== null">
      <VerseComponent
        v-for="(verseItem, index) in result.verses"
        :key="index"
        :verse="verseItem.verse"
        :text="verseItem.text"
      />
    </div>
  </div>
</template>

<script setup>
import { ref } from 'vue'
import axios from 'axios'
import VerseComponent from '../components/VerseComponent.vue'

//skapar två reaktiva variable
const inputVerse = ref('')
const result = ref(null)

function fetchBibleVerse() {
  axios
    .get(`https://bible-api.com/${inputVerse.value}`) //hämtar bibelvers
    .then((response) => {
      result.value = response.data
    })
    .catch((error) => {
      console.error('API get failed', error)
    })
}
</script>

<style lang="scss" scoped></style>
