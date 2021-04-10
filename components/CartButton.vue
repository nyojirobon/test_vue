<template>
  <v-btn
    :to="`${to}`"
    color="primary"
    elevation="2"
    fab
    fixed
    bottom
    right
    nuxt
  >
    <v-icon color="black">{{icon}}</v-icon>
  </v-btn>
</template>

<script>
export default {
  data () {
    return {
      icon: 'fas fa-shopping-basket',
      to: '/cart'
    }
  }
}
</script>
