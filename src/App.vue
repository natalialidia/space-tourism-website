<script>

	import baseHeader from "@/components/base-header.vue";

	export default {
		components: {
			'base-header': baseHeader
		}
	}

</script>

<template>

	<base-header id="navbar"></base-header>

	<router-view></router-view>

</template>

<style lang="scss">
	@import 'assets/styles/style';

	#navbar {
		position: absolute;
		z-index: 100;
		top: 40px;
		left: 0;
		right:0;
	}
</style>
