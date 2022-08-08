<template>
	<LandingPageComponent/>
</template>

<script>
import LandingPageComponent from './components/LandingPageComponent.vue'

export default {
	name: 'App',
	components: {
		LandingPageComponent
	}
}
</script>

<style lang="scss">
@font-face {
	font-family: 'Rubik';
	src: url('./assets/fonts/Rubik-Regular.woff2') format('woff2');
}
#app {
	font-family: 'Rubik';
	-webkit-font-smoothing: antialiased;
	-moz-osx-font-smoothing: grayscale;
	color: #2c3e50;
}
</style>
