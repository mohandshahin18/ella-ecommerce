<template>
  <div class="banner">
    <div class="parent">
      <v-container>
        <v-row>
          <v-col cols="5">
            <div class="cont">
              <h3><span>Huge Saving</span> on UHD Televisions</h3>
              <p>Sale up to 70% on seleted items*</p>
              <v-hover>
                <template v-slot:default="{ isHovering, props }">
                  <v-btn
                    :variant="isHovering ? 'elevated' : 'outlined'"
                    rounded="xl"
                    v-bind="props"
                    height="50"
                    min-width="164"
                    >Shop Now</v-btn
                  >
                </template>
              </v-hover>
            </div>
          </v-col>
        </v-row>
      </v-container>
    </div>
  </div>
</template>

<script setup></script>

<style lang="scss" scoped>
.banner {
  .parent {
    height: 430px;
    background: url(../../assets/images/banner-bg.jpg) no-repeat center center;
    background-size: cover;
    .cont {
      padding: 45px 0 0 40px;
      color: #fff;
      h3 {
        font-size: 45px;
        font-weight: 900;
        margin-bottom: 20px;
        span {
          color: #10ffda;
        }
      }
      p {
        font-size: 18px;
        margin-bottom: 30px;
      }
    }
  }
}
</style>
