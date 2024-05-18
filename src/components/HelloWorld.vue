<script setup lang="ts">
import { ref, watch } from "vue";

const isContentShown = ref(false);

const props = defineProps({
  count: Number,
});

const open = () => (isContentShown.value = true);

console.log(props.count);

defineExpose({
  open,
});

watch(
  () => props.count,
  (old, newCount) => {
    console.log(old, newCount, "props.count");
  }
);

console.log("props.count", () => props.count);
</script>

<template>
  {{ count }}
  <div v-if="isContentShown">oanhhuynh</div>
</template>
