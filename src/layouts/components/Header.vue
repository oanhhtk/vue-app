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
  padding: 0.5rem;
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
  border-radius: 0.5rem;
  border: 1px solid transparent;
  padding: 0.5rem;
  font-size: 1em;
  font-weight: 500;
  font-family: inherit;
  cursor: pointer;
  transition: border-color 0.25s;
  color: #273566;
  background: #eff2f5;
}

@media (max-width: 576px) {
  header {
    flex-direction: column;
    justify-content: start;
    gap: 4px;
    padding: 0.5rem;
  }
  nav.nav {
    gap: 8px;
    display: flex;
    justify-content: space-between;
    & a {
      background: unset;
      color: #eff2f5;
      padding: 4px;
    }
  }
}
</style>
