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
              <v-btn :to="`${item.to}`" class="text-capitalize" text nuxt>{{item.title}}</v-btn>
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
          title: 'about',
          to: '/about'
        },
        {
          title: 'promotion',
          to: '/promotion'
        },
        {
          title: 'shop',
          to: '/product'
        },
        {
          title: 'our store',
          to: '/store'
        },
      ]
    }
  }
}
</script>
