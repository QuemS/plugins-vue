<template>
  <div>
    <div class="title"><h1>Suspense method</h1></div>
    <card-user-sceleton />
    <div class="title"><h1>Stable method</h1></div>
    <div>
      <profile-card-skeleton v-if="loader" />
      <card-user :get-loader="getLoader" v-show="!loader"></card-user>
    </div>
    <div class="title"><h1>Loaded style</h1></div>
    <v-loader class="content_center" />
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
.content_center {
  display: flex;
  justify-content: center;
}
</style>
