<template lang="html">
	<div>
		<p>Vista de usuarios</p>
		<ul v-for="user in users">
			<li>
				{{user.name}}
			</li>
		</ul>
	</div>
</template>

<script>

import axios from 'axios'

	export default {
		data(){
			return {
				users: []
			}
		},
		mounted(){
			axios.get('https://jsonplaceholder.typicode.com/users')
			.then(response => this.users = response.data)
		}
	}
</script>

<style lang="css">
</style>