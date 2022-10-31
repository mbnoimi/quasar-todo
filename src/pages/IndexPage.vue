<template>
  <q-page class="row">
    <q-card class="col-xs-12">
      <q-toolbar>
        <q-input
          dense
          placeholder="Search"
          borderless
          class="full-width"
          :model-value="search"
        >
          <template #append>
            <q-icon name="mdi-magnify" />
          </template>
        </q-input>
      </q-toolbar>
      <q-list bordered>
        <q-item>
          <q-item-section side>
            <q-checkbox :model-value="true" />
          </q-item-section>
          <q-item-section> Go shopping </q-item-section>
          <q-item-section side>
            <q-btn size="sm" round flat icon="mdi-delete"></q-btn>
          </q-item-section>
        </q-item>
      </q-list>
    </q-card>
    <q-page-sticky position="bottom" :offset="[0, 18]">
      <q-btn fab icon="mdi-plus" color="secondary" />
    </q-page-sticky>
  </q-page>
</template>

<script setup lang="ts">
import { ref } from 'vue';

const search = ref('');
</script>
