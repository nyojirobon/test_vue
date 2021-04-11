<template>
  <div class="card-container text-center pr-10 mx-auto">
    <v-img :src="`${src}`"></v-img>
    <v-card :color="`${backgroundColor}`">
      <div
        :class="`card-text d-flex align-end pa-3 text-h5 text-left font-weight-medium ${color}--text`"
      >{{text}}</div>
    </v-card>
  </div>
</template>

<style scoped>
.card-container {
  height: 100%;
  max-width: 300px;
  position: relative;
}

.v-image {
  height: 100%;
  border-radius: 10% !important;
}

.v-card {
  height: calc(50% + 20px);
  width: calc(50% - 25px);
  position: absolute;
  top: 50%;
  left: calc(50% + 10px);
  border-radius: 10% !important;
}

.v-card .card-text {
  height: 100%;
}
</style>

<script>
export default {
  props: {
    src: {
      type: String,
      default: '',
      required: true,
    },
    text: {
      type: String,
      default: '',
      required: true,
    },
    color: {
      type: String,
      default: 'white',
      required: false,
    },
    backgroundColor: {
      type: String,
      default: 'primary',
      required: false,
    }
  }
}
</script>
