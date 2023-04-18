<script>
	import '../app.postcss';
	import { fade } from 'svelte/transition';

	export let router;
</script>

<main transition:fade>
	<slot />
</main>

<style>
	main {
		position: absolute;
		top: 0;
		left: 0;
		right: 0;
		bottom: 0;
	}
</style>
