<template>
  <div>
    <q-input v-model="date" filled type="date" hint="Native date" id="data" />
    <q-input v-model="text" :dense="dense" id="nomeEvento" />

    <div class="q-pa-md">
      <div class="q-gutter-md row items-start">
        <q-input filled v-model="color" class="my-input">
          <template v-slot:append>
            <q-icon name="colorize" class="cursor-pointer">
              <q-popup-proxy
                cover
                transition-show="scale"
                transition-hide="scale"
              >
                <q-color v-model="color" />
              </q-popup-proxy>
            </q-icon>
          </template>
        </q-input>
      </div>
    </div>
    <q-input v-model="text" :dense="dense" id="categoria" />

    <div class="q-pa-md">
      <q-btn-dropdown color="primary" label="Dropdown Button">
        <q-list>
          <q-item clickable v-close-popup @click="onItemClick">
            <q-item-section>
              <q-item-label>Estudos</q-item-label>
            </q-item-section>
          </q-item>

          <q-item clickable v-close-popup @click="onItemClick">
            <q-item-section>
              <q-item-label>Trabalho</q-item-label>
            </q-item-section>
          </q-item>

          <q-item clickable v-close-popup @click="onItemClick">
            <q-item-section>
              <q-item-label>Todos</q-item-label>
            </q-item-section>
          </q-item>

          <q-item clickable v-close-popup @click="onItemClick">
            <q-item-section>
              <q-item-label>Casa</q-item-label>
            </q-item-section>
          </q-item>
        </q-list>
      </q-btn-dropdown>
    </div>
  </div>

  <div>
    <q-btn label="Submit" type="submit" color="primary" />
    
  </div>
  
</template>
<script>

export default {};
</script>
<style></style>
