<script setup>
	import {ref, onMounted} from "vue";
	const currentLabel = ref('');
	const projectsLabel = ref('projects');
	const socialsLabel = ref('socials');
	const trackersLabel = ref('trackers');

	const projects = [
		['rencher', 'a game manager for Ren\'Py visual novels', 'https://github.com/danatationn/rencher'],
		['twotoned', 'a gimmicky skin for osu!', 'https://osu.ppy.sh/community/forums/topics/2062665?n=1'],
		['quixotic', 'a monochrome minimalistic skin for quaver', 'https://steamcommunity.com/sharedfiles/filedetails/?id=3119237347'],
		['fml', 'a uzdoom add-on for people that don\'t use mouselook', 'https://forum.zdoom.org/viewtopic.php?t=80594'],
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
		// ['mal', 'danatationn', 'https://myanimelist.net/profile/danatationn'],
		['vndb', 'u288771', 'https://vndb.org/u288771'],
	];
</script>

<template>
	<body>
		<h1> {{ projectsLabel }}</h1>
		<ul>
			<li v-for="project in projects"
				@mouseover="projectsLabel=project[1]"
				@mouseleave="projectsLabel='projects'">
				<a :href="project[2]"> {{project[0]}} </a>
			</li>
		</ul>

		<h1> {{ socialsLabel }}</h1>
		<ul>
			<li v-for="social in socials"
				@mouseover="socialsLabel=social[1]"
				@mouseleave="socialsLabel='socials'">
				<a :href="social[2]"> {{social[0]}} </a>
			</li>
		</ul>

		<h1> {{ trackersLabel }}</h1>
		<ul>
			<li v-for="tracker in trackers"
			    @mouseover="trackersLabel=tracker[1]"
			    @mouseleave="trackersLabel='trackers'">
				<a :href="tracker[2]"> {{tracker[0]}} </a>
			</li>
		</ul>

		<h5>© copyright 2026</h5>
	</body>
</template>

<style scoped>
</style>
