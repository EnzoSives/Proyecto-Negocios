<template>
  <q-card class="my-card" flat bordered>
    <q-img :src="business.image" class="q-mb-sm" />
    <q-card-section>
      <div class="text-h6">{{ business.name }}</div>
      <div>{{ business.description }}</div>
      <div class="text-subtitle2">{{ business.category }}</div>
      <div>{{ business.address }}</div>
    </q-card-section>
  </q-card>
</template>

<script>
export default {
  name: 'BusinessCard',
  props: {
    business: {
      type: Object,
      required: true,
    },
  },
};
</script>

<style lang="sass" scoped>
.text-h6
  font-size: 18px
  font-weight: 600
.my-card
  width: 100%
  max-width: 300px
</style>
