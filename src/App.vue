<script setup>
	import {ref} from "vue";
	const currentUsername = ref('');
	
	var socials = [
		['twitter', '@danatationn', 'https://x.com/danatationn'],
		['vndb', 'u288771', 'https://vndb.org/u288771'],
		['github', '@danatationn', 'https://github.com/danatationn'],
		['reddit', 'u/danatationn', 'https://reddit.com/user/danatationn'],
		['osu', 'drunkromanian', 'https://osu.ppy.sh/users/36007819'],
		['discord', '@danatationn', 'https://discord.com/users/1282386549685878864'],
		['email', 'lemontasteicetea@pm.me', 'mailto:lemontasteicetea@pm.me']
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
