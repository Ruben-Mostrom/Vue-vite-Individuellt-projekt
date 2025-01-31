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

<style scoped></style>
