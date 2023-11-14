<template>
  <q-layout view="lHh Lpr lFf" class="bg-white">
    <topo @toggleMenu="toggleLeftDrawer"/>
    <q-page-container>
      <div class="p-2" v-if="route == 'Tarefas'">
        
        <tarefas />
        <evento/>
      </div>
      <div class="p-2" v-if="route == 'Categorias'">
        <categorias />
        
      </div>
    </q-page-container>
  </q-layout>
</template>

<script>
import topo from "./components/topo.vue"
import tarefas from "./components/tarefas.vue"
import categorias from "./components/categorias.vue"
import evento from "./components/evento.vue"

export default {
  components: { topo, tarefas, categorias, evento },
  data() {
    return {
      leftDrawerOpen: true,
      route: 'Tarefas'
    }
  },
  methods: {
    toggleLeftDrawer () {
      this.$refs.menuopcoesref.toggleLeftDrawer()
    },
    selectItem(item) {
      console.log(item);
      this.route = item.label
    }
  },
}
</script>
<style></style>