<template>
  <q-input
    rounded
    outlined
    v-model="query"
    placeholder="Buscar..."
    @input="onSearch"
    dense
    class="buscador"
  >
    <template v-slot:append>
      <q-avatar class="icon-container">
        <q-icon name="search" />
      </q-avatar>
    </template>
  </q-input>
</template>

<script>
export default {
  data() {
    return {
      query: '',
    };
  },
  methods: {
    onSearch() {
      console.log('Buscando:', this.query);
    },
  },
};
</script>

<style lang="css">
.buscador {
  width: 100%;
  max-width: 600px;
  margin: auto;
  transition:
    box-shadow 0.3s ease,
    transform 0.2s ease;
}

.buscador:focus-within {
  box-shadow: 0 4px 12px rgba(0, 0, 0, 0.1);
  transform: scale(1.02);
  border-radius: 20px;
}

.icon-container {
  background-color: #007bff; /* Azul principal */
  color: white;
  border-radius: 20px;
}

.q-input:hover {
  border-color: #007bff;
  border-radius: 20px;
}

.q-input__control {
  font-size: 16px;
  padding: 12px;
}

.q-icon {
  font-size: 18px;
}
</style>
