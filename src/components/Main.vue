<template>
	<main>
		<div v-for="(album, index) in albums" :key="index">{{ album.title }}</div>
	</main>
</template>

<script>
import axios from 'axios';
export default {
	name: 'Main',
	data() {
		return {
			URL: 'https://flynn.boolean.careers/exercises/api/array/music',
			albums: [],
		};
	},
	methods: {
		fetchAlbums() {
			axios.get(this.URL).then((result) => {
				//console.log(result.data.response);
				this.albums = result.data.response;
				console.log(this.albums);
			});
		},
	},
	mounted() {
		this.fetchAlbums();
	},
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss"></style>
