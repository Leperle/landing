<template>
	<div>
		<Hero />
		<Features />
		<Roadmap />
		<Listing />
<!--		<CallToAction />-->
	</div>
</template>

<script>
export default {
	layout: 'default',
	mounted() {
		this.initGrid();
	}
}
</script>
