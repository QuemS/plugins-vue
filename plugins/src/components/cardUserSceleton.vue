<template>
  <Suspense>
    <template #default>
      <card-user />
    </template>
    <template #fallback>
      <profile-card-skeleton-vue />
    </template>
  </Suspense>
</template>

<script>
import cardUser from './cardUser.vue'
import ProfileCardSkeletonVue from './ProfileCardSkeleton.vue'

export default {
  name: 'cardUserSceleton',
  components: {
    cardUser,
    ProfileCardSkeletonVue
  }
}
</script>

<style></style>
