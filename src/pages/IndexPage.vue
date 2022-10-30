<template>
  <q-page padding>
    <q-select
      v-model="selected"
      label="numbers"
      filled
      :options="['one', 'two', 'three']"
    ></q-select>
  </q-page>
</template>

<script setup lang="ts">
import { ref } from 'vue';

const selected = ref('');
</script>
