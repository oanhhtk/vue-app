<script setup lang="ts"></script>

<template>
  <header>
    <div class="app-logo">
      <img src="https://i.imgur.com/sOCVfKv.png" alt="logo vue" />
    </div>
    <nav class="nav">
      <a>Indie Game</a>
      <a>Entry game</a>
      <a>Commuinity</a>
    </nav>
  </header>
</template>

<style scoped lang="scss">
.app-logo {
  display: flex;
  align-items: center;
  gap: 8px;
}

header {
  display: flex;
  justify-content: space-between;
  align-items: center;
}

.nav {
  display: flex;
  gap: 10px;
}

nav.nav a {
  border-radius: 8px;
  border: 1px solid transparent;
  padding: 0.4em 1em;
  font-size: 1em;
  font-weight: 500;
  font-family: inherit;
  cursor: pointer;
  transition: border-color 0.25s;
  color: #273566;
  background: #fff;
}
</style>
