<script setup lang="ts">
import { CardType } from "../Main.vue";
import Card from "./Card.vue";

defineProps<{
  list: CardType[];
}>();
</script>

<template>
  <div class="card-list">
    <Card class="card-item" v-for="card in list" :card />
  </div>
</template>

<style lang="scss">
.card-list {
  display: grid;
  gap: 1rem;
}

.card-item {
  box-shadow: 0 4px 8px rgba(38, 38, 38, 0.2);
  padding: 0.5rem;
  margin: 0.5rem;
  & img {
    aspect-ratio: 3/2;
    width: 100%;
    object-fit: cover;
  }
}
</style>
