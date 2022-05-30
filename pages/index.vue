<template>
  <div>
    <v-parallax
      class="parallax-1 view-height-100"
      :src="require('~/assets/images/splash_ink_bg_1.png')"
    >
      <v-row align="center" justify="center" style="color: black">
        <v-spacer />
        <v-col cols="6">
          <v-row justify="center">
            <div class="position-relative">
              <img
                class="logo position-relative position-top-left"
                :src="require('~/assets/images/logo.png')"
              />
              <img
                class="logo position-absolute position-top-left animate-wink"
                :src="require('~/assets/images/keyhole.png')"
              />
            </div>
          </v-row>
          <v-row justify="center">
            <h1>Mix01 StudiO</h1>
          </v-row>
          <v-row>
            <v-divider />
          </v-row>
          <v-row justify="center">
            <h4>數位設計 / 全端開發</h4>
          </v-row>
          <v-row justify="center">
            <div class="animate-float-box_large-button">
              <v-btn
                icon
                large
                plain
                class="position-absolute animate-float"
                @click="$vuetify.goTo('#parallax-2', options)"
              >
                <FontAwesomeIcon icon="sort-down" />
              </v-btn>
            </div>
          </v-row>
        </v-col>
        <v-spacer />
      </v-row>
    </v-parallax>
    <v-parallax
      id="parallax-2"
      class="parallax-2"
      :src="require('~/assets/images/smoke_black_bg.png')"
    >
      <v-spacer />
      <v-row>
        <v-col md="6" sm="12">
          <div class="padding-30">
            <h1>ZERO mix ONE</h1>
            <h2>可能性 x 創造力</h2>
            <div>
              = We make dreams come true.
              <br />
              <br />
              能創工作室(Mix01)內容內容內容內容內容內容內容內容內容內容內容內容內容，
              內容內容內容內容內容內容內容內容內，容內容內容內容內容
              內容內容內容內容內容內容內容內容內容內容內容內容內容
              內容內容內容內容內容內容內容內容內容內容，內容內容內容
              內容內容內容內容內容內容內容內容內容內容內容內容內容。
              <br />
              <br />
              內容內容內容
              內容內容內容內容內容內容內容內容內容內容內容內容內容。
            </div>
          </div>
        </v-col>
      </v-row>
      <v-spacer />
    </v-parallax>
    <v-parallax
      id="parallax-3"
      class="parallax-3"
      :src="require('~/assets/images/smoke_white_rotate_bg.png')"
    >
    </v-parallax>
  </div>
</template>

<script>
export default {
  name: 'IndexPage',
  data() {
    return {
      goToOptions: {
        duration: 300,
        offset: 0,
        easing: 'easeInOutCubic',
      },
    }
  },
}
</script>