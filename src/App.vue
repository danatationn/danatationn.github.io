<script setup>
	var socials = [
		['twitter', '@danatationn', 'https://x.com/danatationn'],
		['vndb', 'u288771', 'https://vndb.org/u288771/ulist?vnlist=1'],
		['github', '@danatationn', 'https://github.com/danatationn'],
		['reddit', 'u/danatationn', 'https://reddit.com/user/danatationn'],
		['osu', 'drunkromanian', 'https://osu.ppy.sh/users/36007819'],
		['discord', '@danatationn', 'https://discord.com/users/1282386549685878864'],
		['email', 'lemontasteicetea@pm.me', 'mailto:lemontasteicetea@pm.me']
	]
</script>

<template>
	<h1>site under construction</h1>

	<ul>
		<li v-for="social in socials"> 
			<a :href="social[2]"> {{social[0]}} </a> 
		</li>
	</ul>

	<h5>© copyright 2025</h5>
</template>

<style scoped>
</style>
