<template>
  <q-page class="flex flex-center" padding>
    <div class="full-width" style="max-width: 300px">
      <h5 class="q-my-md text-center">Login</h5>
      <q-card>
        <q-form>
          <q-card-section>
            <q-input
              label="email"
              placeholder="email@example.com"
              class="q-mb-md"
              type="email"
              filled
            />

            <q-input label="password" class="q-mb-sm" type="password" filled />

            <q-checkbox label="remember me" :model-value="true" />
          </q-card-section>
          <q-btn label="login" class="full-width" color="primary" />
        </q-form>
      </q-card>
    </div>
  </q-page>
</template>
