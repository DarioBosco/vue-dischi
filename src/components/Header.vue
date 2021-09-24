<template>
	<header class="d-flex justify-content-between align-items-center">
		<div class="image-box">
			<img :src="logo" alt="" />
		</div>
		<label for="genreSelect">Seleziona il genere:</label>
		<select v-model="selectedGenre" name="genreSelect" id="genreSelect" @change="$emit('changedSelected', selectedGenre)">
			<option selected value="all">Tutti i generi</option>
			<option value="rock">Rock</option>
			<option value="pop">Pop</option>
			<option value="jazz">Jazz</option>
			<option value="metal">Metal</option>
		</select>
	</header>
</template>

<script>
export default {
	name: 'Header',
	data() {
		return {
			logo: 'https://upload.wikimedia.org/wikipedia/commons/7/75/Spotify_icon.png',
			selectedGenre: 'all',
		};
	},
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
@import '../styles/general';
@import '../styles/mixins';
header {
	height: 70px;
	width: 100%;
	background-color: $bg-light;
	.image-box {
		height: 100%;
		width: 10%;
		@include center(vertical);
		margin-left: 10px;
		img {
			height: 100%;
			padding: 10px;
		}
	}
}
</style>
