<script>
	import Header from '../components/Header.svelte';
	import Circles from '../components/CirclesBottom.svelte';
	import Layout from './+layout.svelte';
	import router from './+layout.svelte';
</script>

<svelte:head>
	<title>Uriel Navarta</title>
	<link rel="apple-touch-icon" sizes="180x180" href="/apple-touch-icon.png" />
	<link rel="icon" type="image/png" sizes="32x32" href="/favicon-32x32.png" />
	<link rel="icon" type="image/png" sizes="16x16" href="/favicon-16x16.png" />
	<link rel="manifest" href="/site.webmanifest" />
</svelte:head>

<Layout {router}>
	<main>
		<Header />
		<div class="body">
			<p class="name">Uriel Navarta.</p>
			<p class="under-text">
				Frontend Developer based in Mendoza, Argentina obsessed with making stunning web pages.
			</p>
		</div>
		<div class="circles">
			<Circles />
		</div>
	</main>
</Layout>

<style>
	@import url('https://fonts.googleapis.com/css2?family=Inter:wght@400;700&display=swap');

	.name {
		margin-top: 150px;
		margin-left: 50px;
		font-size: 125px;
		font-family: 'Inter', sans-serif;
		font-weight: 700;
		max-width: 500px;
		line-height: 1em;
		color: #2f2f2f;
		transition: all 0.3s ease;
		transform: scale(1);
		color: #2f2f2f;
	}
	.body {
		margin-left: 50px;
	}
	.name:hover {
		transition: all 0.3s ease;
		transform: scale(1.2);
		color: #ff748d;
	}

	.under-text {
		max-width: 550px;
		font-size: 20px;
		font-weight: 400;
		margin-top: 20px;
		font-family: 'Inter', sans-serif;
		font-weight: 700;
		color: #2f2f2f;
		margin-left: 55px;
	}
	.circles {
		max-height: 50px;
		margin-left: 50px;
	}
	/* Define the `fade` transition */
	.fade {
		transition: opacity 0.5s ease;
	}

	/* Define the starting and ending states of the `fade` transition */
	.fade-enter {
		opacity: 0;
	}
	.fade-enter-active {
		opacity: 1;
	}
	.fade-exit {
		opacity: 1;
	}
	.fade-exit-active {
		opacity: 0;
	}

	@media screen and (max-width: 700px) {
		* {
			margin: 0;
			padding: 0;
			box-sizing: border-box;
		}
		.body {
			margin: 0 auto;
			padding: 150px 0 0 0;
			display: block;
		}

		main {
			background-image: url('./../assets/blurry-gradient-haikei.svg');
			background-repeat: no-repeat;
			background-size: cover;
			min-width: 800px;
			min-height: 1800px;
			margin: 0 auto;
			display: block;
		}
		.name {
			margin: 0 auto;
			padding: 0;

			display: flex;
			justify-content: center;
			align-items: center;
			text-align: center;
		}
		.body {
			margin-left: 0;
			max-width: 900px;
		}

		.under-text {
			margin-left: 0;
			font-size: 40px;
			text-align: center;
			display: flex;
			justify-content: center;
			align-items: center;
			max-width: 900px;
		}
		.circles {
			margin-left: 0;
		}
	}
</style>
