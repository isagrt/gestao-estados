<script>
import { count } from "console";
import { mapStores, mapState, mapActions } from "pinia";
export default {
  data() {
    return {
      nome: "Isadora",
      nome_editar: "Isadora",
    };
  },
  computed: {
    ...mapStores(useCounterStore),
    ...mapActions(useCounterStore), (count, doubleCount)
  },
};
</script>

<template>
  <main>
    <h1>Pagina Main</h1>
    <input type="text" v-model="nome_editar" />
    <button @click="nome = nome_editar">Enviar</button>
    <h2>{{ nome }}</h2>
  </main>
</template>
