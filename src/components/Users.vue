<template>
	<div class="container users">
		<h1 class="users__heading">Users</h1>
		<div class="row row-cols-1 row-cols-sm-2">
			<div class="col" v-for="user in users" :key="user.id">
				User {{ user.id }}
			</div>
		</div>
	</div>
</template>

<script>
import data from '../data';

export default {
	name: 'Users',
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
			font-size: 40px;
			font-weight: 700;
			line-height: 1.13;
			letter-spacing: -1px;
			text-align: center;
			margin-bottom: 40px;

			@media (min-width: 576px) {
				font-size: 64px;
			}

			@media (min-width: 992px) {
				font-size: 80px;
			}
		}
	}
</style>
