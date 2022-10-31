<template>
  <q-layout view="hHh Lpr lFf">
    <q-header elevated>
      <q-toolbar>
        <q-btn
          flat
          dense
          round
          icon="mdi-menu"
          aria-label="Menu"
          @click="toggleLeftDrawer"
        />

        <q-toolbar-title> Todo </q-toolbar-title>

        <!-- <div>Quasar v{{ $q.version }}</div> -->
        <q-btn icon="mdi-logout" flat padding="2px"></q-btn>
      </q-toolbar>
    </q-header>

    <q-drawer v-model="leftDrawerOpen" show-if-above bordered>
      <q-list>
        <!-- FIXME: unable to apply manual style -->
        <q-item
          class="bg-grey-3"
          dense
          style="border-bottom: 2px; border-color: chartreuse"
        >
          <q-item-section> Lists </q-item-section>
          <q-item-section side>
            <q-btn round flat icon="mdi-plus"> </q-btn>
          </q-item-section>
        </q-item>
        <q-item clickable>
          <q-item-section side>
            <q-icon name="mdi-shopping"></q-icon>
          </q-item-section>
          <q-item-section> Shopping List </q-item-section>
          <q-item-section side> 12 </q-item-section>
        </q-item>
      </q-list>
    </q-drawer>

    <q-page-container>
      <router-view />
    </q-page-container>
  </q-layout>
</template>

<script setup lang="ts">
import { ref } from 'vue';

const leftDrawerOpen = ref(false);

function toggleLeftDrawer() {
  leftDrawerOpen.value = !leftDrawerOpen.value;
}
</script>
