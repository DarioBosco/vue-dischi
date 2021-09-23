<template>
	<div>
		<div class="me-4">
			<label for="genre" class="text-white">Seleziona il genere:</label>
			<select name="genre" id="genre" class="ms-3">
				<option selected value="">Tutti i generi</option>
				<option value="">Rock</option>
				<option value="">Pop</option>
				<option value="">Classic</option>
			</select>
		</div>
	</div>
</template>

<script>
export default {
	name: 'Search',
};
</script>

<style scoped lang="scss">
@import '../styles/general';
@import '../styles/mixins';
</style>
