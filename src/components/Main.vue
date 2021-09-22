<template>
	<main class="d-flex justify-content-center align-items-center flex-wrap">
		<Album v-for="(album, index) in albums" :key="index" :album="album" />
	</main>
</template>

<script>
import Album from './Album.vue';
import axios from 'axios';
export default {
	name: 'Main',
	components: {
		Album,
	},
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
<style scoped lang="scss">
@import '../styles/general';
@import '../styles/mixins';
main {
	background-color: $bg-dark;
	min-height: calc(100vh - 70px);
	width: 60%;
	margin: 0 auto;
}
</style>
