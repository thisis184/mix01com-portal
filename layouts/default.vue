<template>
  <v-app>
    <v-app-bar dark dense collapse fixed>
      <div>{{ title }}</div>
      <v-spacer />
      <v-btn icon @click.stop="drawer = !drawer">
        <v-icon>mdi-menu</v-icon>
      </v-btn>
    </v-app-bar>

    <v-navigation-drawer v-model="drawer" dark temporary fixed>
      <v-list>
        <v-list-item>
          <v-list-item-action>
            <v-icon light> mdi-repeat </v-icon>
          </v-list-item-action>
          <v-list-item-title>Switch drawer (click me)</v-list-item-title>
        </v-list-item>
      </v-list>
    </v-navigation-drawer>

    <v-main>
      <v-container fluid pa-0>
        <Nuxt />
      </v-container>
    </v-main>

    <v-footer dark absolute app style="background-color: black; padding: 0">
      <div style="width: 100%; height: 300px">link list</div>
      <v-divider style="margin: 1px; border-color: rgba(255, 255, 255, 0.5)" />
      <div style="width: 100%">footer</div>
    </v-footer>
  </v-app>
</template>

<script>
export default {
  name: 'DefaultLayout',
  data() {
    return {
      title: 'mix01 Studio.',
      drawer: false,
      items: [
        {
          icon: 'mdi-apps',
          title: 'Welcome',
          to: '/',
        },
        {
          icon: 'mdi-chart-bubble',
          title: 'Inspire',
          to: '/inspire',
        },
      ],
    }
  },
}
</script>
