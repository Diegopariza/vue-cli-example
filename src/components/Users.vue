<template>
  <div class="container users">
    <h1 class="users__heading">Users</h1>
    <div class="row row-cols-2">
      <div class="col" v-for="user in users" :key="user.id">
        <User :name="user.name" :avatar="user.avatar" :bio="user.bio" />
      </div>
    </div>
  </div>
</template>

<script>
import data from '../data';
import User from './User';

export default {
	name: 'Users',
	components: {
		User
	},
  data() {
    return {
      users: data
    }
  }
}
</script>

<style scoped lang="scss">
.users {
  margin-top: 60px;

  &__heading {
    font-size: 80px;
    font-weight: 700;
    line-height: 1.13;
    letter-spacing: -1px;
    text-align: center;
    margin-bottom: 40px;
  }
}
</style>
