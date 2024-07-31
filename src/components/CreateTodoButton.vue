<template>
  <q-btn @click="handleButtonClick" />
</template>

<script setup>
import { useQuasar } from 'quasar'

const $q = useQuasar()

const handleButtonClick = () => {
  $q.dialog({
    title: 'Create Todo',
    prompt: {
      model: '',
      type: 'text', // optional
    },
    cancel: true,
    persistent: true,
  })
    // .onOk((data) => {
    //   console.log('>>>> OK, received', data)
    // })
    .onOk(createTodo)
    .onCancel(() => {
      console.log('>>>> Cancel')
    })
    .onDismiss(() => {
      console.log('I am triggered on both OK and Cancel')
    })
}

const createTodo = (data) => {
  console.log('adding todo: ', data)
  $q.notify({
    message: 'Todo created!',
    icon: 'mdi-check',
    color: 'positive',
  })
}
</script>
