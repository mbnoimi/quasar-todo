<template>
  <q-btn @click="clickTodoButton" />
</template>

<script setup lang="ts">
import { useQuasar } from 'quasar';
const $q = useQuasar();
function clickTodoButton() {
  $q.dialog({
    title: 'Create Todo',
    message: 'Input your todo content',
    prompt: {
      model: '',
      type: 'text', // optional
    },
    cancel: true,
    persistent: true,
  })
    .onOk(createTodo)
    .onCancel(() => {
      // console.log('>>>> Cancel')
    });
}

function createTodo() {
  $q.notify({
    message: 'Todo Created!',
    icon: 'mdi-check',
    color: 'positive',
  });
}
</script>
