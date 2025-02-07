<template>
  <div>
    <input v-model="inputVerse" placeholder="search for a bibleverse" />
    <input type="button" @click="fetchBibleVerse" value="search" />
    <div v-if="result !== null">
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
