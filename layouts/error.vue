<template>
  <v-app>
    <v-parallax
      class="parallax-1 view-height-100"
      :src="require('~/assets/images/splash_ink_bg_1.png')"
    >
      <v-row justify="center" align="center" class="text-center">
        <v-col style="color: black">
          <h1 v-if="error.statusCode === 404">
            {{ pageNotFound }}
          </h1>
          <h1 v-else>
            {{ otherError }}
          </h1>
          <br />
          <NuxtLink to="/">
            <FontAwesomeIcon icon="house" /> Home page
          </NuxtLink>
        </v-col>
      </v-row>
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

<style scoped>
h1 {
  font-size: 20px;
}
</style>
