<template>
  <q-page class="q-pa-md">
    <q-tabs v-model="selectedCategory" class="text-teal" align="left" dense>
      <q-tab
        v-for="category in categories"
        :key="category"
        :name="category"
        :label="category"
      />
    </q-tabs>

    <q-separator class="q-my-md" />

    <div class="q-gutter-md">
      <BusinessCard
        v-for="business in filteredBusinesses"
        :key="business.id"
        :business="business"
      />
    </div>
  </q-page>
</template>

<script>
import BusinessCard from 'src/components/BussinesCard.vue';

export default {
  components: { BusinessCard },
  data() {
    return {
      selectedCategory: 'All Categories',
      categories: [
        'Todas',
        'Restaurantes',
        'Kioscos',
        'Electrodomesticos',
        'Repuestos',
        'Alimentos',
      ],
      businesses: [
        {
          id: 1,
          category: 'Restaurantes',
          name: 'Café del Centro',
          description: 'Delicious coffee and pastries',
          address: '123 Main St',
          image: 'link_to_image1',
        },
        {
          id: 2,
          category: 'Repuestos',
          name: 'Librería El Progreso',
          description: 'Books and stationery',
          address: '456 Second St',
          image: 'link_to_image2',
        },
        // Agrega más negocios aquí
      ],
    };
  },
  computed: {
    filteredBusinesses() {
      if (this.selectedCategory === 'Todas') {
        return this.businesses;
      }
      return this.businesses.filter(
        (business) => business.category === this.selectedCategory,
      );
    },
  },
};
</script>

<style scoped>
.text-teal {
  color: teal;
}
</style>
