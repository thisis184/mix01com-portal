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
            <img class="logo" :src="require('~/assets/images/logo.png')" />
          </v-row>
          <v-row justify="center">
            <h1>MIX01 STUDIO</h1>
          </v-row>
          <v-row>
            <v-divider />
          </v-row>
          <v-row justify="center">
            <h4>數位設計 / 全端開發</h4>
          </v-row>
        </v-col>
        <v-spacer />
      </v-row>
      <v-row />
    </v-parallax>
  </div>
</template>

<script>
export default {
  name: 'IndexPage',
}
</script>