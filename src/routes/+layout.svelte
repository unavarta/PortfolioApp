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
	
		background-image: url('./../assets/blurry-gradient-haikei.svg');
		background-repeat: no-repeat;
		background-size: cover;
	
	}

	@media screen and (max-width: 700px) {
		main {
			min-width: 800px;
			min-height: 1800px;
			margin: 0 auto;
			
		}
	}
</style>
