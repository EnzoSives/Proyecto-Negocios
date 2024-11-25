<template>
  <q-layout view="hHh Lpr lff" class="shadow-2 rounded-borders">
    <q-header elevated>
      <q-toolbar class="justify-between">
        <q-btn flat @click="drawer = !drawer" round dense icon="menu" />
        <search-component></search-component>
        <q-btn flat @click="drawer = !drawer" round dense icon="user" />
      </q-toolbar>
    </q-header>

    <q-drawer
      v-model="drawer"
      show-if-above
      bordered
      :width="250"
      :breakpoint="500"
    >
      <q-scroll-area class="fit">
        <q-list padding class="menu-list">
          <q-item clickable v-ripple to="/">
            <q-item-section avatar>
              <q-item-label><q-icon name="home" /> Home </q-item-label>
            </q-item-section>
          </q-item>

          <q-separator></q-separator>

          <q-item-label header> Rubros </q-item-label>
          <q-item active clickable v-ripple to="/negocios">
            <q-item-section avatar>
              <q-icon name="star" />
            </q-item-section>

            <q-item-section> Negocios </q-item-section>
          </q-item>
        </q-list>
      </q-scroll-area>
    </q-drawer>

    <q-page-container>
      <router-view />
    </q-page-container>
  </q-layout>
</template>

<script setup lang="ts">
import { ref } from 'vue';
import SearchComponent from 'src/components/SearchComponent.vue';
// import EssentialLink, {
//   type EssentialLinkProps,
// } from 'components/EssentialLink.vue';

// const linksList: EssentialLinkProps[] = [
//   {
//     title: 'Docs',
//     caption: 'quasar.dev',
//     icon: 'school',
//     link: 'https://quasar.dev',
//   },
//   {
//     title: 'Github',
//     caption: 'github.com/quasarframework',
//     icon: 'code',
//     link: 'https://github.com/quasarframework',
//   },
//   {
//     title: 'Discord Chat Channel',
//     caption: 'chat.quasar.dev',
//     icon: 'chat',
//     link: 'https://chat.quasar.dev',
//   },
//   {
//     title: 'Forum',
//     caption: 'forum.quasar.dev',
//     icon: 'record_voice_over',
//     link: 'https://forum.quasar.dev',
//   },
//   {
//     title: 'Twitter',
//     caption: '@quasarframework',
//     icon: 'rss_feed',
//     link: 'https://twitter.quasar.dev',
//   },
//   {
//     title: 'Facebook',
//     caption: '@QuasarFramework',
//     icon: 'public',
//     link: 'https://facebook.quasar.dev',
//   },
//   {
//     title: 'Quasar Awesome',
//     caption: 'Community Quasar projects',
//     icon: 'favorite',
//     link: 'https://awesome.quasar.dev',
//   },
// ];

const drawer = ref(false);

// function toggleLeftDrawer() {
//   leftDrawerOpen.value = !leftDrawerOpen.value;
// }
</script>
