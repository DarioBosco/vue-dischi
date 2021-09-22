<template>
	<header>
		<div class="image-box">
			<img :src="logo" alt="" />
		</div>
	</header>
</template>

<script>
export default {
	name: 'Header',
	data() {
		return {
			logo: 'https://upload.wikimedia.org/wikipedia/commons/7/75/Spotify_icon.png',
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
	background-color: grey;
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
