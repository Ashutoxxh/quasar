<template>
  <q-page
    class="bg-primary window-height window-width row justify-center items-center"
  >
    <div class="column">
      <div class="row text-center">
        <h5 class="text-h5 text-white q-my-md">LogIn Form</h5>
      </div>
      <div class="row">
        <q-card square bordered class="q-pa-lg shadow-1">
          <q-card-section>
            <q-form class="q-gutter-md">
              <q-input
                square
                filled
                clearable
                v-model="email"
                type="email"
                label="email"
                :rules="[(val) => !!val || 'Email is required']"
              />
              <q-input
                square
                filled
                clearable
                v-model="password"
                type="password"
                label="password"
                :rules="[(val) => !!val || 'password is required']"
              />
            </q-form>
          </q-card-section>
          <q-card-actions class="q-px-md">
            <q-btn
              unelevated
              color="light-green-7"
              size="lg"
              class="full-width"
              label="Login"
            />
          </q-card-actions>
          <q-card-section class="text-center q-pa-none">
            <p class="text-grey-6">Not reigistered? Created an Account</p>
          </q-card-section>
        </q-card>
      </div>
    </div>
  </q-page>
</template>

<script setup>
import { ref } from "vue";

const email = ref("");
const password = ref("");
</script>

<style>
.q-card {
  width: 360px;
}
</style>
