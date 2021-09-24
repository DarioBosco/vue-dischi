<template>
	<div id="app">
		<Header />
		<Main />
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
	props : {
		album: Object,
	}
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
