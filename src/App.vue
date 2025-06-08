<script setup>
	import {ref} from "vue";
	const currentLabel = ref('');
	
	const projects = [
		['rencher', 'a wip game manager for ren\'py visual novels', 'https://github.com/danatationn/rencher'],
		['twotoned', 'a gimmicky skin for osu!', 'https://osu.ppy.sh/community/forums/topics/2062665?n=1'],
		['quixotic', 'a monochrome minimalistic skin for quaver', 'https://steamcommunity.com/sharedfiles/filedetails/?id=3119237347'],
		['game saves', 'not really a project, it\'s just my game saves', 'https://drive.google.com/drive/u/0/folders/1FU32ms9k0orRqWZWYPxa2XpawBniZYpi'],
	];
	
	const socials = [
		['discord', '@danatationn', 'https://discord.com/users/1282386549685878864'],
		['email', 'lemontasteicetea@proton.me', 'mailto:lemontasteicetea@proton.me'],
		['github', '@danatationn', 'https://github.com/danatationn'],
		//['instagram', 'danatationn', 'https://www.instagram.com/danatationn/'],
		['reddit', 'u/danatationn', 'https://reddit.com/user/danatationn'],
		['steam', 'danatationn', 'https://steamcommunity.com/id/danatationn'],
		['twitter', '@danatationn', 'https://x.com/danatationn'],
	];

	const trackers = [
		['last.fm', 'drunkromanian', 'https://www.last.fm/user/drunkromanian'],
		['mal', 'danatationn', 'https://myanimelist.net/profile/danatationn'],
		['vndb', 'u288771', 'https://vndb.org/u288771'],
	];
</script>

<template>
	<body>
		<h1>projects</h1>
		<ul>
			<li v-for="project in projects"
				@mouseover="currentLabel=project[1]"
				@mouseleave="currentLabel=''">
				<a :href="project[2]"> {{project[0]}}</a>
			</li>
		</ul>
		
		<h1>socials</h1>
		<ul>
			<li v-for="social in socials"
				@mouseover="currentLabel=social[1]"
				@mouseleave="currentLabel=''"> 
				<a :href="social[2]"> {{social[0]}} </a> 
			</li>
		</ul>

		<h1>trackers</h1>
		<ul>
			<li v-for="tracker in trackers"
			    @mouseover="currentLabel=tracker[1]"
			    @mouseleave="currentLabel=''">
				<a :href="tracker[2]"> {{tracker[0]}} </a>
			</li>
		</ul>

		<h3>{{ currentLabel }}</h3>
		
		<h5>© copyright 2025</h5>
	</body>
</template>

<style scoped>
</style>
