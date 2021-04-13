<template>
  <v-app light>
    <Header />
    <v-main>
      <nuxt />
    </v-main>
    <Footer />
    <CartButton v-if="this.$route.path !== '/cart'" />
  </v-app>
</template>

<script>
import Header from "@/components/Header.vue";
import Footer from "@/components/Footer.vue";
import CartButton from "@/components/CartButton.vue";
export default {
  components: {
    Header,
    Footer,
    CartButton,
  }
}
</script>
