<template>
  <div class="user">
    <h2 class="user__name">{{ name }}</h2>
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

  &__name {
    font-size: 32px;
    font-weight: 700;
    line-height: 1.19;
    letter-spacing: -0.8px;
  }
}
</style>