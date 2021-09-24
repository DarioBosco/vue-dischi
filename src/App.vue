<template>
	<div id="app">
		<Header @changedSelected="updateCurrentSearch" />
		<Main :currentGenre="currentGenre" />
	</div>
</template>

<script>
import Header from './components/Header.vue';
import Main from './components/Main.vue';

export default {
	name: 'App',
	components: {
		Main,
		Header,
	},
	data() {
		return {
			currentGenre: '',
		};
	},
	methods: {
		updateCurrentSearch(result) {
			this.currentGenre = result;
		},
	},
	created() {
		this.updateCurrentSearch('all');
	},
};
</script>

<style lang="scss">
@import './styles/general';
@import './styles/mixins';
* {
	margin: 0;
	padding: 0;
	box-sizing: border-box;
}

body {
	background-color: $bg-dark;
}
</style>
