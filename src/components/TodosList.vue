<template>
  <q-list>
    <q-item>
      <q-item-section side>
        <UpdateTodoCheckbox />
      </q-item-section>
      <q-item-section> Go shopping </q-item-section>
      <q-item-section side>
        <DeleteTodoButton icon="mdi-delete" size="sm" flat round />
      </q-item-section>
    </q-item>
  </q-list>
</template>

<script setup>
import UpdateTodoCheckbox from 'components/UpdateTodoCheckbox.vue'
import DeleteTodoButton from 'components/DeleteTodoButton.vue'
</script>
