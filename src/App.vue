<template>
	<app-header />
	<div class="box">
		<h1 class="box__title">132</h1>
	</div>
</template>

<script>
import AppHeader from './components/AppHeader.vue'
export default {
	name: 'App',
	components: { AppHeader },
}
</script>

<style lang="scss">
.box {
	&__title {
		color: red;
	}
}
</style>
