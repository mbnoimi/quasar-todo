<template>
  <q-page class="flex flex-center" padding>
    <div class="full-width" style="max-width: 300px">
      <h5 class="q-my-md text-center">Login</h5>
      <q-card>
        <q-form>
          <q-card-section>
            <q-input
              placeholder="email@domain.com"
              filled
              label="E-Mail"
              :model-value="username"
              type="email"
            >
            </q-input>
          </q-card-section>
          <q-card-section>
            <q-input
              filled
              label="Password"
              :model-value="password"
              type="password"
            >
            </q-input>
          </q-card-section>
          <q-card-section>
            <q-checkbox dense label="Remember Me" :model-value="true" />
          </q-card-section>
        </q-form>
        <q-btn color="primary" class="full-width" label="Login"></q-btn>
      </q-card>
    </div>
  </q-page>
</template>

<script setup lang="ts">
import { ref } from 'vue';
const username = ref('');
const password = ref('');
</script>
