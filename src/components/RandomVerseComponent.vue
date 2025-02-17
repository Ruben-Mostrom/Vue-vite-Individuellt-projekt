<script setup>
defineProps({
  text: String,
  book: String,
  chapter: Number,
  verse: Number,
})
</script>

<template>
  <div class="verse-container">
    <h1 v-if="book && chapter && verse">
      {{ book }} {{ chapter }}:{{ verse }}
    </h1>
    <p v-if="text">{{ text }}</p>
  </div>
</template>
