<template>
  <v-app>
    <v-parallax
      class="parallax-1 view-height-100"
      :src="require('~/assets/images/splash_ink_bg_1.png')"
    >
      <v-row justify="center" align="center" class="text-center">
        <v-col cols="6" style="color: black">
          <v-row justify="center">
            <FontAwesomeIcon class="logo" icon="bomb" />
          </v-row>
          <v-row justify="center">
            <h1 v-if="error.statusCode === 404">
              {{ pageNotFound }}
            </h1>
            <h1 v-else>
              {{ otherError }}
            </h1>
          </v-row>
          <v-row>
            <v-divider />
          </v-row>
          <v-row justify="center">
            <NuxtLink to="/">
              <FontAwesomeIcon icon="house" /> Home page
            </NuxtLink>
          </v-row>
        </v-col>
      </v-row>
      <v-row class="parallax-1-bottom-space" />
    </v-parallax>
  </v-app>
</template>

<script>
export default {
  name: 'EmptyLayout',
  layout: 'empty',
  props: {
    error: {
      type: Object,
      default: null,
    },
  },
  data() {
    return {
      pageNotFound: '404 Not Found',
      otherError: 'An error occurred',
    }
  },
  head() {
    const title =
      this.error.statusCode === 404 ? this.pageNotFound : this.otherError
    return {
      title,
    }
  },
}
</script>
