<template>
  <div class="offers pt-9">
    <v-container fluid style="max-width: 93% !important">
      <v-row>
        <v-col cols="4" class="px-5" style="object-fit: cover">
          <v-hover>
            <template v-slot="{ isHovering, props }">
              <div class="parent" v-bind="props">
                <img
                  src="../../assets/images/playstations.webp"
                  :style="isHovering ? 'transform: scale(1.06)' : ''"
                />
              </div>
            </template>
          </v-hover>
        </v-col>
        <v-col cols="4" class="px-5" style="object-fit: cover">
          <v-hover>
            <template v-slot="{ isHovering, props }">
              <div class="parent" v-bind="props">
                <img
                  src="../../assets/images/headset.webp"
                  :style="isHovering ? 'transform: scale(1.06)' : ''"
                />
              </div>
            </template>
          </v-hover>
        </v-col>
        <v-col cols="4" class="px-5" style="object-fit: cover">
          <v-hover>
            <template v-slot="{ isHovering, props }">
              <div class="parent" v-bind="props">
                <img
                  src="../../assets/images/chairs.webp"
                  :style="isHovering ? 'transform: scale(1.06)' : ''"
                />
              </div>
            </template>
          </v-hover>
        </v-col>

        <v-col cols="6" class="px-5" style="object-fit: cover">
          <v-hover>
            <template v-slot="{ isHovering, props }">
              <div class="parent" v-bind="props">
                <img
                  src="../../assets/images/iphones.webp"
                  :style="isHovering ? 'transform: scale(1.06)' : ''"
                />
              </div>
            </template>
          </v-hover>
        </v-col>
        <v-col cols="6" class="px-5" style="object-fit: cover">
          <v-hover>
            <template v-slot="{ isHovering, props }">
              <div class="parent" v-bind="props">
                <img
                  src="../../assets/images/laptops.webp"
                  :style="isHovering ? 'transform: scale(1.06)' : ''"
                />
              </div>
            </template>
          </v-hover>
        </v-col>
      </v-row>
    </v-container>
  </div>
</template>

<script setup></script>

<style lang="scss" scoped>
.offers {
  background-color: #f5f5f5;
  .parent {
    overflow: hidden;
    border-radius: 5px;
    height: 100%;
    cursor: pointer;
    img {
      width: 100%;
      height: 100%;
      transition: transform 0.64s ease;
    }
  }
}
</style>
