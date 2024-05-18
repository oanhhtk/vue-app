<script setup lang="ts">
import { CardType } from "../Main.vue";

defineProps<{
  card: CardType;
}>();
</script>

<template>
  <div>
    <img :src="card?.src" />
    <p class="truncate-text bold">
      {{ card?.title }}
    </p>
  </div>
</template>

<style lang="scss" scoped>
.truncate-text {
  --max-line: 1;
  display: -webkit-box;
  -webkit-line-clamp: var(--max-line);
  -webkit-box-orient: vertical;
  overflow: hidden;
}
.bold {
  font-weight: bold;
}
</style>
