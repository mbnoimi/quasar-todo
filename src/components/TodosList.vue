<template>
  <q-list>
    <q-item>
      <q-item-section side>
        <UpdateTodoCheckbox />
      </q-item-section>
      <q-item-section> Go shopping </q-item-section>
      <q-item-section side>
        <DeleteTodoButton
          size="sm"
          round
          flat
          icon="mdi-delete"
        ></DeleteTodoButton>
      </q-item-section>
    </q-item>
  </q-list>
</template>

<script setup lang="ts">
import DeleteTodoButton from './DeleteTodoButton.vue';
import UpdateTodoCheckbox from './UpdateTodoCheckbox.vue';
</script>
