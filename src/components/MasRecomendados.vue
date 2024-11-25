<template>
  <div class="q-pa-md">
    <div class="row q-col-gutter-lg q-row-gutter-lg">
      <q-card class="my-card" v-for="book in books" :key="book.id">
        <img :src="book.image" alt="Book cover" class="book-image" />

        <q-card-section>
          <div class="text-h6">{{ book.title }}</div>
          <div class="text-subtitle2">by {{ book.author }}</div>
        </q-card-section>

        <q-card-section class="q-pt-none">
          {{ book.description }}
        </q-card-section>
      </q-card>
    </div>
  </div>
</template>

<script>
export default {
  setup() {
    const books = [
      {
        id: 1,
        title: 'Our Changing Planet',
        author: 'John Doe',
        image: 'https://cdn.quasar.dev/img/mountains.jpg',
        description:
          'A book about the environmental changes happening on our planet.',
      },
      {
        id: 2,
        title: 'Climate Change Today',
        author: 'Jane Smith',
        image: 'https://cdn.quasar.dev/img/mountains.jpg',
        description:
          'An in-depth look at the effects of climate change globally.',
      },
      {
        id: 3,
        title: 'Sustainability Practices',
        author: 'Mary Johnson',
        image: 'https://cdn.quasar.dev/img/mountains.jpg',
        description: 'A guide to living sustainably in modern times.',
      },
      {
        id: 4,
        title: 'Green Energy',
        author: 'James Brown',
        image: 'https://cdn.quasar.dev/img/mountains.jpg',
        description: 'Exploring renewable energy sources for a cleaner future.',
      },
      {
        id: 5,
        title: 'Urban Wildlife',
        author: 'Robert Green',
        image: 'https://cdn.quasar.dev/img/mountains.jpg',
        description:
          'Understanding the interaction between wildlife and urbanization.',
      },
    ];

    return { books };
  },
};
</script>

<style lang="sass" scoped>
.row
  display: flex
  flex-wrap: wrap
  justify-content: space-between
  gap: 24px // Espacio adicional entre tarjetas

.my-card
  flex: 1 1 calc(25% - 34px) // Ancho ajustado para compensar el gap
  display: flex
  flex-direction: column
  align-items: center
  border-radius: 8px

.book-image
  width: 100%
  height: auto
  padding-right: 20px
</style>
