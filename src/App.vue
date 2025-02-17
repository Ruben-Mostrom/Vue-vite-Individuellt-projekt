<script setup></script>

<template>
  <nav>
    <ul>
      <li>
        <RouterLink to="/">Search for Bible verse</RouterLink>
      </li>
      <li>
        <RouterLink to="/about">Random bible verse</RouterLink>
      </li>
    </ul>
  </nav>
  <main>
    <RouterView />
  </main>
</template>

<style scoped>
nav > ul {
  display: flex;
  flex-direction: row;
  gap: 4rem;
  list-style-type: none;
  justify-content: center;
  padding: 0;
}

nav li {
  background-color: brown;
  border-radius: 0.5rem;
  padding: 0.5rem;
}
</style>
