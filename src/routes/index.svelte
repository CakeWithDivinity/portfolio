<script context="module" lang="ts">
	export const prerender = true;
</script>

<script lang="ts">
	import Hero from '$lib/hero.svelte';
</script>

<section class="hero-section">
	<Hero />
</section>

<style lang="scss">
	section {
		width: 100%;
		height: 100vh;
	}

	.hero-section {
		position: relative;
	}
</style>
