<template>
  <v-container>
    <v-row>
      <v-col cols=12 md=6>
        <v-row class="mb-3">
          <v-col cols=12>
            <div class="text-h5 font-weight-medium mx-auto">
              Lassana Delights Your Daily Coffee Experience
            </div>
          </v-col>
          <v-col cols=12>
            <div class="text-body2">
              Lassana is a Hong Kong local brand that specialize in coffee and fresh bakery. We are here to provide excellent food service that inspire you everyday.
            </div>
          </v-col>
        </v-row>
      </v-col>
      <v-col cols=12 md=6>
        <v-img :src="`${topImage.src}`" contain max-height="250px"></v-img>
      </v-col>
    </v-row>
    <v-row class="my-3">
      <v-col cols=12>
        <v-carousel cycle :show-arrows="false" :hide-delimiter-background="true">
          <v-carousel-item
            v-for="(image,i) in carouselImages"
            :key="i"
            :src="image.src"
          ></v-carousel-item>
        </v-carousel>
      </v-col>
    </v-row>
    <v-row class="my-3">
      <v-col
        class="my-3"
        cols=12
        md=4
        v-for="(card,i) in textImageCards"
        :key="i"
      >
        <TextImageCard v-bind="card" />
      </v-col>
    </v-row>
    <v-row class="mt-3" justify="center">
      <v-col cols=12>
        <v-row>
          <v-col cols=12>
            <div class="text-subtitle1 font-weight-medium">
              For Further Information About Lassana Service including Coffee and Fresh Bakery
            </div>
          </v-col>
        </v-row>
        <v-row align="center" justify="start">
          <v-col cols=12>
            <v-btn :to="`${contactButton.to}`" large depressed class="primary text-h6" nuxt>{{contactButton.text}}</v-btn>
          </v-col>
        </v-row>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
import TextImageCard from '~/components/TextImageCard.vue'

export default {
  components: {
    TextImageCard
  },
  data() {
    return {
      topImage: {
        src: 'https://www.lassana.hk/_nuxt/img/ee7e9ce.png'
      },
      carouselImages: [
        {
          src: 'https://api-eshop.lassana.hk/api/attachments/60138da7d930b6001e077e67.exlarge.webp'
        },
        {
          src: 'https://api-eshop.lassana.hk/api/attachments/60138da7d930b6001e077e53.large.webp'
        },
        {
          src: 'https://api-eshop.lassana.hk/api/attachments/60138da7d930b6001e077e67.exlarge.webp'
        }
      ],
      textImageCards: [
        {
          src: 'https://www.lassana.hk/_nuxt/img/36a3ef1.png',
          text: 'Our Coffee',
          backgroundColor: 'black'
        },
        {
          src: 'https://www.lassana.hk/_nuxt/img/70ec6fb.png',
          text: 'Our Pastry'
        },
        {
          src: 'https://www.lassana.hk/_nuxt/img/aca2482.png',
          text: 'Our Food',
          backgroundColor: 'light-green darken-4'
        }
      ],
      contactButton: {
        to: '/contact',
        text: 'Contact Us'
      }
    }
  }
}
</script>
