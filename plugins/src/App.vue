<template>
  <div>
    <div class="title"><h1>Suspense method</h1></div>
    <card-user-sceleton />
    <div class="title"><h1>Stable method</h1></div>
    <div>
      <profile-card-skeleton v-if="loader" />
      <card-user :get-loader="getLoader" v-show="!loader"></card-user>
    </div>
    <v-loader />
  </div>
</template>

<script>
import cardUserSceleton from './components/cardUserSceleton.vue'
import VLoader from './components/VLoader.vue'
import cardUser from './components/newSceleton/cardUser.vue'
import ProfileCardSkeleton from './components/ProfileCardSkeleton.vue'

export default {
  data() {
    return {
      iten: '',
      loader: true
    }
  },
  methods: {
    getLoader(value) {
      console.log(value)
      this.loader = value
    }
  },

  components: {
    cardUserSceleton,
    VLoader,
    cardUser,
    ProfileCardSkeleton
  }
}
</script>

<style>
.title {
  text-align: center;
}
</style>
