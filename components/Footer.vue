<template>
    <v-footer
      :absolute="!fixed"
      color="black"
      app
    >
      <v-container fluid>
        <v-row align="center" justify="space-between">
          <v-col align="center" class="hidden-sm-and-down">
            <v-row align="center" justify="start">
              <v-col cols="auto">
                <div class="white--text text-h6">
                  Want To Know Lassana Better?
                </div>
              </v-col>
            </v-row>
            <v-row align="center" justify="start">
              <v-col v-for="(item, i) in sns" :key="i" cols="auto">
                <v-btn :to="`${item.to}`" icon nuxt>
                  <v-icon color="white" large>{{item.icon}}</v-icon>
                </v-btn>
              </v-col>
            </v-row>
            <v-row align="center" justify="start">
              <v-col cols="auto">
                <div class="white--text text-subtitle-1">
                  Customer Service: 63930906
                </div>
              </v-col>
            </v-row>
          </v-col>
          <v-col cols=12 md=3>
            <nuxt-link :to="`${image.to}`">
              <v-img :src="`${image.src}`" max-height="80px" contain=true></v-img>
            </nuxt-link>
          </v-col>
       </v-row>
        <v-row align="center" justify="center">
          <v-col cols="auto">
            <div class="white--text text-subtitle-2">
              ©️ {{ new Date().getFullYear() }} By LASSANA Limited
            </div>
          </v-col>
        </v-row>
      </v-container>
    </v-footer>
</template>

<script>
export default {
  data () {
    return {
      image: {
        src: '/v.png',
        to: '/'
      },
      sns: [
        {
          icon: 'fab fa-facebook',
          to: ''
        },
        {
          icon: 'fab fa-instagram',
          to: ''
        }
      ]
    }
  }
}
</script>
