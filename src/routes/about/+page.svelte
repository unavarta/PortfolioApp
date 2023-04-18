<script>
	import Header from '../../components/Header.svelte';
	import Circles from '../../components/CirclesBottom.svelte';
	import Profile from '../../assets/yo.jpeg';
	import Background from '../../assets/blurry-gradient-haikei.svg';
	import Layout from '../+layout.svelte';
	import router from '../+layout.svelte';
</script>

<main>
	<Layout {router}>
		<Header />
		<div class="body">
			<div class="text">
				<p class="name">
					My name is Uriel Navarta Triveño, I am a 22-year-old junior Computer Science student.
					<br />
					<br />
					I enjoy both coding and designing aesthetically pleasing websites.
					<br />
					<br />
					In addition, I enjoy learning about video game design and data science.
				</p>
			</div>
			<div class="image">
				<img src={Profile} alt="" />
			</div>
		</div>
		<div class="circles">
			<Circles />
		</div>
	</Layout>
</main>

<style>
	.name {
		font-size: 34px;
		font-family: 'Inter', sans-serif;
		font-weight: 700;
		max-width: 700px;
		line-height: 1em;
		color: #2f2f2f;
	}
	.text {
		display: flex;
		flex-direction: column;
		justify-content: center;
	}

	.body {
		display: grid;
		grid-template-columns: 1fr 1fr;
		gap: 100px;
		width: 1400px;
		margin-top: 150px;
		margin-left: 100px;
	}

	.image {
		max-width: 500px;
		display: flex;
		justify-content: center;
		align-items: center;
	}
	img {
		max-width: 320px;
		max-height: 320px;
		border-radius: 50%;
		border: 5px solid #ff748d;
		transform: scale(1); /* decrease the size of the image on hover */
		transition: all 0.3s ease;
	}

	img:hover {
		transform: scale(1.5); /* Increase the size of the image on hover */
		transition: all 0.3s ease;
	}

	.circles {
		max-height: 50px;
		margin-left: 50px;
	}

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
	
</style>
