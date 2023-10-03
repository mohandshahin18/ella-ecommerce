<template>
  <div class="layout">
    <v-layout class="position-relative">
      <!-- start Cart Drawer -->
      <CartDrawer />
      <!-- end Cart Drawer -->

      <v-main style="padding-top: 146px">
        <slot></slot>
      </v-main>

      <!-- start navbar -->
      <AppNav />
      <!-- end navbar -->

      <!-- start footer -->
      <AppFooter />
      <!-- end footer -->

      <!--strat fixed nav -->
      <FixedNav v-if="showFixedNav" />
      <!-- end fixed nav -->
    </v-layout>
  </div>
</template>

<script>
import AppNav from "./AppNav.vue";
import AppFooter from "./AppFooter.vue";
import CartDrawer from "./CartDrawer.vue";
import FixedNav from "./FixedNav.vue";
export default {
  components: {
    AppNav,
    AppFooter,
    CartDrawer,
    FixedNav,
  },
  data: () => ({
    showFixedNav: false,
  }),
  mounted() {
    window.addEventListener("scroll", this.handleScroll);
  },
  methods: {
    handleScroll() {
      const scrollThreshold = 250;

      if (window.scrollY > scrollThreshold) {
        this.showFixedNav = true;
      } else {
        this.showFixedNav = false;
      }
    },
  },
  beforeUnmount() {
    window.removeEventListener("scroll", this.handleScroll);
  },
};
</script>
