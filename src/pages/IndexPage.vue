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
      <TodosList bordered> </TodosList>
    </q-card>
    <q-page-sticky position="bottom" :offset="[0, 18]">
      <CreateTodoButton fab glossy icon="mdi-plus" color="secondary" />
    </q-page-sticky>
  </q-page>
</template>

<script setup lang="ts">
import CreateTodoButton from 'src/components/CreateTodoButton.vue';
import { ref } from 'vue';
import TodosList from 'src/components/TodosList.vue';

const search = ref('');
</script>
