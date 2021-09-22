<template>
	<div id="album" class="d-flex flex-column align-items-center text-center">
		<div class="image-box">
			<img class="img-fluid" :src="album.poster" alt="" />
		</div>
		<div class="details">
			<h2 class="title mt-4">{{ album.title }}</h2>
			<p class="detail m-0">{{ album.author }}</p>
			<p class="detail m-0">{{ album.year }}</p>
		</div>
	</div>
</template>

<script>
export default {
	name: 'Album',
	props: {
		album: Object,
	},
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
@import '../styles/general';
@import '../styles/mixins';

#album {
	background-color: $bg-light;
	height: 400px;
	padding: 20px;
	margin: 20px;
	width: calc(100% / 5 - 80px);
	.image-box {
		height: 150px;
		width: 150px;
	}

	.title {
		color: white;
		font-size: 1.5rem;
		text-transform: uppercase;
	}

	.detail {
		color: grey;
	}
}
</style>
