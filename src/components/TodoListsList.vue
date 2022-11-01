<template>
  <q-list>
    <!-- ---------- Header ------------- -->
    <!-- FIXME: unable to apply manual style -->
    <q-item
      class="bg-grey-3"
      dense
      style="border-bottom: 2px; border-color: chartreuse"
    >
      <q-item-section> Lists </q-item-section>
      <q-item-section side>
        <CreateTodoListButton round flat icon="mdi-plus">
        </CreateTodoListButton>
      </q-item-section>
    </q-item>
    <!-- ------------- Content ------------- -->
    <q-item clickable>
      <q-item-section side>
        <q-icon name="mdi-shopping"></q-icon>
      </q-item-section>
      <q-item-section class="text-grey-9"> Shopping List </q-item-section>
      <q-item-section side> 12 </q-item-section>
    </q-item>
  </q-list>
</template>

<script setup lang="ts">
import CreateTodoListButton from './CreateTodoListButton.vue';
//
</script>
