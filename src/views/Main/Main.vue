<script setup lang="ts">
import { ref } from "vue";
import CardList from "./components/CardList.vue";

export type CardType = {
  id: string | number;
  title: string;
  src: string;
};

const list = ref<CardType[]>(
  Array.from({ length: 20 }).map((_, index) => ({
    id: index,
    title: `${index}. Card title Lorem ipsum dolor sit amet consectetur adipisicing elit. Ex, esse pariatur corrupti ea quidem, molestias praesentium, unde consequatur repellendus aspernatur consequuntur quibusdam eos sint autem quisquam vero provident ab exercitationem eligendi. Dolore ipsum esse quam ducimus debitis, asperiores at dignissimos eum consectetur id, praesentium mollitia maxime tempore saepe sed iure ipsa possimus nam velit temporibus accusamus explicabo? Quisquam, maiores? Non vero porro labore, pariatur quidem officiis temporibus repellendus nisi a tenetur corporis eveniet deleniti suscipit! Nobis ullam debitis ipsa a eveniet reiciendis excepturi cupiditate molestias corporis adipisci suscipit, hic et nisi, molestiae quibusdam repellendus eos veniam iste similique libero nostrum?`,
    src:
      index % 2 === 0
        ? `https://i.imgur.com/unmma82.jpeg`
        : `https://i.imgur.com/2MM9Jqo.png`,
  }))
);
</script>

<template>
  <main>
    <h1>Photo Cards</h1>
    <CardList :list />
  </main>
</template>
