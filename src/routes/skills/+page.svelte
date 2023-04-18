<script>
	import Header from '../../components/Header.svelte';
	import Circles from '../../components/CirclesBottom.svelte';
	import { fade } from 'svelte/transition';
	import Icon from '@iconify/svelte';

	import Layout from '../+layout.svelte';
	import router from '../+layout.svelte';
</script>

<main>
	<Layout {router}>
		<Header />
		<div class="body">
			<div class="grid-container">
				<div class="cardad">
					<div class="card">
						<div class="branding-card">
							<Icon
								class="icon"
								icon="tabler:brand-svelte"
								color="#2f2f2f"
								width="70"
								height="70"
							/>
							<h2>Svelte</h2>
						</div>
						<div class="description">
							<p>
								Used to build powerful lightweight Apps. Take a look at my <a
									href="https://checklist-sveltekit.vercel.app/"
									target="_blank">Checklist App</a
								>.
							</p>
						</div>
					</div>
				</div>
				<div class="cardad">
					<div class="card">
						<div class="branding-card">
							<Icon icon="simple-icons:tailwindcss" color="#2f2f2f" width="70" height="70" />
							<h2>TailwindCSS</h2>
						</div>
						<div class="description">
							<p>
								TailwindCSS is a nice approach to making websites pop. Will soon be uploading apps
								that showcase it's usefulness.
							</p>
						</div>
					</div>
				</div>
				<div class="cardad">
					<div class="card">
						<div class="branding-card">
							<Icon icon="mdi:language-typescript" color="#2f2f2f" width="70" height="70" />
							<h2>TypeScript</h2>
						</div>
						<div class="description">
							<p>
								TypeScript is a better way of writing web code, it's scalable for bigger projects
								and overall more precise.
							</p>
						</div>
					</div>
				</div>
				<div class="cardad">
					<div class="card">
						<div class="branding-card">
							<Icon
								icon="material-symbols:computer-outline-rounded"
								color="#2f2f2f"
								width="70"
								height="70"
							/>
							<h2>Other Technologies I have Some Knwoledge on</h2>
						</div>
						<div class="description">
							<div class="items">
								<Icon icon="mdi:language-java" color="#2f2f2f" width="70" height="70" />
								<Icon icon="mdi:language-csharp" color="#2f2f2f" width="70" height="70" />
								<Icon icon="la:react" color="#2f2f2f" width="70" height="70" />
								<Icon icon="ph:file-sql" color="#2f2f2f" width="70" height="70" />
							</div>
						</div>
					</div>
				</div>
			</div>
		</div>
		<div class="circles">
			<Circles />
		</div>
	</Layout>
</main>

<style>
	@import url('https://fonts.googleapis.com/css2?family=Inter:wght@400;700&display=swap');

	.circles {
		max-height: 50px;
		margin-left: 50px;
	}
	.branding-card h2 {
		line-height: 1em;
	}
	.icon:hover {
		color: #ff748d;
		transition: 0.2s ease;
	}

	.items {
		display: flex;
		gap: 10px;
		justify-content: space-around;
	}
	a:hover {
		text-decoration: underline #ff748d;
		transition: 0.2s ease;
		color: #ff748d;
	}
	.grid-container {
		max-width: 1200px;
		margin: 0 auto;
		display: grid;
		grid-template-columns: repeat(2, 1fr);
		grid-template-rows: repeat(2, auto);
		gap: 20px;
	}
	.description {
		margin-left: 20px;
		margin-top: 20px;
		margin-right: 20px;
		font-size: 20px;
		font-family: 'Inter', sans-serif;
		font-weight: 700;
		color: #2f2f2f;
	}
	.cardad {
		display: flex;
		justify-content: center;
	}
	.card {
		margin-top: 20px;
		width: 500px;
		height: 220px;
		background-color: #fff;
		border-radius: 10px;
		box-shadow: 0px 4px 6px rgba(0, 0, 0, 0.1);
	}

	.card h2 {
		font-size: 24px;
		font-weight: 500;
		color: #333;
		font-family: 'Inter', sans-serif;
		font-weight: 700;
	}
	.branding-card {
		display: flex;
		align-items: center;
		margin-left: 20px;
		margin-top: 20px;
		gap: 10px;
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
