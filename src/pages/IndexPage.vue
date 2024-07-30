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

      <TodosList bordered />
    </q-card>

    <div class="col-xs-3">
      <q-toolbar class="bg-primary">
        <CreateTodoButton
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
import CreateTodoButton from 'components/CreateTodoButton.vue'
import TodosList from 'components/TodosList.vue'

const search = ref('')
</script>
