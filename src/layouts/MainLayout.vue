<template>
  <q-layout view="lHh Lpr lFf">
    <q-page-container>
      <router-view />
    </q-page-container>
     <!-- Mobile Bottom Bar -->
    <q-footer bordered class="bg-white text-primary">
      <q-tabs
        no-caps
        active-color="primary"
        indicator-color="transparent"
        class="text-grey"
      >
        <!-- v-model="tab" -->
        <q-tab>
          <q-icon class="text-dark" size="lg">
            <img src="~assets/Logo.svg" />
          </q-icon>
          <span>Home</span>
        </q-tab>
        <q-tab>
          <q-icon class="text-dark" size="lg">
            <img src="~assets/pay.svg" />
          </q-icon>
          <span>Cards</span>
        </q-tab>
        <q-tab>
          <q-icon class="text-dark" size="lg">
            <img src="~assets/Payments.svg" />
          </q-icon>
          <span>Payments</span>
        </q-tab>
        <q-tab>
          <q-icon class="text-dark" size="lg">
            <img src="~assets/Credit.svg" />
          </q-icon>
          <span>Credit</span>
        </q-tab>
        <q-tab>
          <q-icon class="text-dark" size="lg">
            <img src="~assets/Account.svg" />
          </q-icon>
          <span>Profile</span>
        </q-tab>
      </q-tabs>
    </q-footer>
  </q-layout>
</template>

<script>
import { defineComponent, ref } from "vue";

export default defineComponent({
  name: "MainLayout",

  components: {},

  setup() {},
});
</script>
