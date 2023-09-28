<template>
  <div class="darwer">
    <v-navigation-drawer
      color="red"
      v-model="drawer"
      temporary
      location="right"
    >
      <p>
        Lorem ipsum dolor sit amet consectetur adipisicing elit. Labore, natus
        accusamus sit sed est dolor, fuga veritatis officiis deleniti eaque
        error alias asperiores tempora rem. At amet eveniet iste quae?
      </p>
    </v-navigation-drawer>
  </div>
</template>

<script>
export default {
  inject: ["Emitter"],
  data: () => ({
    drawer: false,
  }),
  mounted() {
    this.Emitter.on("openCart", () => {
      this.drawer = true;
    });
  },
};
</script>
<style lang="scss" scoped></style>
