<script setup>
	import {ref} from "vue";
	const currentUsername = ref('');
	
	var socials = [
		['discord', '@danatationn', 'https://discord.com/users/1282386549685878864'],
		['email', 'lemontasteicetea@proton.me', 'mailto:lemontasteicetea@pm.me'],
		['github', '@danatationn', 'https://github.com/danatationn'],
		['instagram', 'danatationn', 'https://www.instagram.com/danatationn/'],
		['last.fm', 'drunkromanian', 'https://www.last.fm/user/drunkromanian'],
		['reddit', 'u/danatationn', 'https://reddit.com/user/danatationn'],
		['steam', 'danatationn', 'https://steamcommunity.com/id/danatationn'],
		['twitter', '@danatationn', 'https://x.com/danatationn'],
		['vndb', 'u288771', 'https://vndb.org/u288771'],
	]
</script>

<template>
	<body>
		<h1>site under construction</h1>
	
		<ul>
			<li v-for="social in socials"
				@mouseover="currentUsername=social[1]"
				@mouseleave="currentUsername=''"> 
				<a :href="social[2]"> {{social[0]}} </a> 
			</li>
		</ul>
		
		<h3>{{currentUsername}}</h3>
		
		<h5>© copyright 2025</h5>
	</body>
</template>

<style scoped>
</style>
