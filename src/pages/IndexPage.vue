<template>
  <q-page class="row">
    <q-card class="col-xs-9">
      <q-toolbar>
        <q-input
          v-model="search"
          placeholder="Search"
          class="full-width"
          borderless
          dense
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
            <q-btn icon="mdi-delete" size="sm" flat round />
          </q-item-section>
        </q-item>
      </q-list>
    </q-card>

    <div class="col-xs-3">
      <q-toolbar class="bg-primary">
        <q-btn
          icon="mdi-plus"
          color="secondary"
          class="q-ml-lg"
          style="margin-bottom: -48px"
          fab
        />
      </q-toolbar>
    </div>
  </q-page>
</template>

<script setup>
import { ref } from 'vue'

const search = ref('')
</script>
