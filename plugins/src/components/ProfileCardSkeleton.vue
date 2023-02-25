<template>
  <div class="profile-card">
    <div class="profile-image">
      <img class="profile-image__img animation" />
    </div>
    <div class="profile-info">
      <span class="animation" />
      <h3 class="animation" />
      <p class="animation" />
    </div>
  </div>
</template>

<script>
export default {
  name: 'ProfileCardSkeleton'
}
</script>

<style scoped>
.animation {
  animation: pulse-bg 1.5s infinite;
}
@keyframes pulse-bg {
  0% {
    background-color: #e6e6e6;
  }
  50% {
    background-color: #b3b2b2;
  }
  100% {
    background-color: #e6e6e6;
  }
}

.profile-card .profile-image__img {
  width: 10%;
  padding-top: 10%;
  border-radius: 50%;
}
.profile-info span {
  min-width: 100px;
  height: 16px;
  display: inline-block;
  background-color: #ddd;
}
.profile-info h3 {
  content: ' ';
  width: 250px;
  height: 24px;
  background-color: #ddd;
  margin: 10px 0;
}
.profile-info p {
  width: 80%;
  background-color: #ddd;
  height: 16px;
  line-height: 140%;
}
</style>
