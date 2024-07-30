<template>
  <q-layout view="hHh Lpr lFf">
    <q-header>
      <q-toolbar>
        <q-btn
          flat
          dense
          round
          icon="mdi-menu"
          aria-label="Menu"
          @click="toggleLeftDrawer"
        />

        <q-toolbar-title> Todo App </q-toolbar-title>

        <q-btn icon="mdi-logout" flat round />
      </q-toolbar>
    </q-header>

    <q-drawer v-model="leftDrawerOpen" show-if-above bordered>
      <q-toolbar class="bg-primary" />

      <q-item class="bg-grey-3">
        <q-item-section>Lists</q-item-section>
        <q-item-section side>
          <CreateTodoListButton icon="mdi-plus" size="sm" flat round />
        </q-item-section>
      </q-item>

      <TodoListsList />
    </q-drawer>

    <q-page-container>
      <router-view />
    </q-page-container>
  </q-layout>
</template>

<script setup>
import { ref } from 'vue'
import CreateTodoListButton from 'components/CreateTodoListButton.vue'
import TodoListsList from 'components/TodoListsList.vue'

const leftDrawerOpen = ref(false)

const toggleLeftDrawer = () => {
  leftDrawerOpen.value = !leftDrawerOpen.value
}
</script>
