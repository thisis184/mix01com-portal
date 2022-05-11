<template>
  <div>
    <v-parallax
      class="view-height"
      :src="require('~/assets/images/splash_ink_bg_1.png')"
    >
      <v-row align="center" justify="center" style="height: 100%; color: black">
        <v-spacer />
        <v-col cols="6">
          <v-row justify="center"><h1>mix01 Studio</h1></v-row>
          <v-row>
            <v-col v-for="n in 3" :key="n" cols="4">
              <v-row justify="center">
                <h3>service title</h3>
              </v-row>
            </v-col>
          </v-row>
          <v-row>
            <v-divider />
          </v-row>
          <v-row justify="center"> slogen </v-row>
        </v-col>
        <v-spacer />
      </v-row>
    </v-parallax>
  </div>
</template>

<script>
export default {
  name: 'IndexPage',
}
</script>

<style>
.v-parallax__image {
  width: 100%;
  bottom: 15%;
}

.view-height {
  height: 100vh !important;
}
</style>