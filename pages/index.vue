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
              <v-btn icon large plain class="position-absolute animate-float">
                <FontAwesomeIcon icon="sort-down" />
              </v-btn>
            </div>
          </v-row>
        </v-col>
        <v-spacer />
      </v-row>
      <v-row />
    </v-parallax>
    <div>0/1整合 無限可能</div>
  </div>
</template>

<script>
export default {
  name: 'IndexPage',
}
</script>