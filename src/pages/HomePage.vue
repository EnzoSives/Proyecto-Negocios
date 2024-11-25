<template>
  <q-page class="items-center justify-evenly">
    <Carousel></Carousel>

    <div class="recomendados" style="padding-left: 20px">
      <h6>Mas recomendados</h6>
      <Recomendados></Recomendados>
    </div>
  </q-page>
</template>

<script setup lang="ts">
import Carousel from 'src/components/CarouselNegocios.vue';
import Recomendados from 'src/components/MasRecomendados.vue';
// import Drawer from 'src/components/DrawerComponent.vue';
</script>
