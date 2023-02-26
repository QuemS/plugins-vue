<template>
  <div>
    <card-user-sceleton />
    <v-loader />
  </div>
</template>

<script>
import cardUserSceleton from './components/cardUserSceleton.vue'
import VLoader from './components/VLoader.vue'

export default {
  components: {
    cardUserSceleton,
    VLoader
  }
}
</script>

<style></style>
