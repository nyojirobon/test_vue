<template>
  <v-app-bar
      height="100px"
      flat
      :absolute="!fixed"
      color="white"
      app
  >
    <v-container fluid>
      <v-row align="center" justify="space-between">
        <v-col cols=12 md=3>
          <nuxt-link :to="`${image.to}`">
            <v-img :src="`${image.src}`" max-height="80px" contain=true></v-img>
          </nuxt-link>
        </v-col>
        <v-col align="center" class="hidden-sm-and-down">
          <v-row no-gutters align="center" justify="end">
            <v-col v-for="(item, i) in items" :key="i" cols="auto">
              <v-btn :to="`${item.to}`" text nuxt>{{item.title}}</v-btn>
            </v-col>
          </v-row>
        </v-col>
      </v-row>
    </v-container>
  </v-app-bar>
</template>

<script>
export default {
  data () {
    return {
      image: {
        src: '/v.png',
        to: '/'
      },
      items: [
        {
          title: 'About',
          to: '/about'
        },
        {
          title: 'Promotion',
          to: '/promotion'
        },
        {
          title: 'Shop',
          to: '/product'
        },
        {
          title: 'Our Store',
          to: '/store'
        },
      ]
    }
  }
}
</script>
