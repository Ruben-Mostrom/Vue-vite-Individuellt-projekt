<script setup>
import { watchEffect } from 'vue'

const props = defineProps({ text: String, verse: Number })

watchEffect(() => {
  console.log(props.verse)
})
</script>

<template>
  <div class="verse-container">
    <h2 v-if="verse">{{ verse }}</h2>
    <p v-if="text">{{ text }}</p>
  </div>
</template>
