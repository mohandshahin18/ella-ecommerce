<template>
  <div class="layout">
    <v-layout class="position-relative">
      <!-- start Cart Drawer -->
      <CartDrawer :drawer="drawer" />
      <!-- end Cart Drawer -->

      <v-main style="padding-top: 146px">
        <slot></slot>
      </v-main>

      <!-- start navbar -->
      <AppNav :drawer="false" />
      <!-- end navbar -->

      <!-- start footer -->
      <AppFooter />
      <!-- end footer -->
    </v-layout>
  </div>
</template>

<script>
import AppNav from "./AppNav.vue";
import AppFooter from "./AppFooter.vue";
import CartDrawer from "./CartDrawer.vue";
export default {
  components: {
    AppNav,
    AppFooter,
    CartDrawer,
  },
  data: () => ({
    drawer: false,
  }),
};
</script>
