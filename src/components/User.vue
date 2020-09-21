<template>
  <div class="user">
    <div class="user__avatar">
      <img :src="avatar" :alt="name" />
    </div>
    <h2 class="user__name">{{ name }}</h2>
    <p class="user__bio">
      {{ bio }}
    </p>
  </div>
</template>

<script>
export default {
  name: 'User',
  props: {
    name: String,
    avatar: String,
    bio: String
  }
}
</script>

<style scoped lang="scss">
.user {
  padding: 30px 110px 30px 30px;

  &__avatar {
    width: 200px;
    height: 200px;
    margin-bottom: 64px;
    border-radius: 50%;
    overflow: hidden;

    img {
      width: 100%;
      height: 100%;
    }
  }

  &__name {
    font-size: 32px;
    font-weight: 700;
    line-height: 1.19;
    letter-spacing: -0.8px;
    margin-bottom: 15px;
  }

  &__bio {
    font-size: 18px;
    font-weight: 400;
    line-height: 1.44;
    letter-spacing: -0.5px;
  }
}
</style>