<script>
	import Logo from '../assets/logo.png';
	import Icon from '@iconify/svelte';
</script>

<main>
	<nav>
		<div class="container">
			<div class="navbar-brand">
				<a href="/"><img src={Logo} alt="Logo" /></a>
			</div>
			<ul class="navbar-nav">
				<li class="nav-item"><a class="" href="/">home</a></li>
				<li class="nav-item"><a href="/skills">skills</a></li>
				<li class="nav-item"><a href="/about">about</a></li>
				<li class="nav-item">
					<a class="git" href="https://github.com/unavarta"
						><Icon
							class="git"
							icon="tabler:brand-github-filled"
							color="#2f2f2f"
							width="40"
							height="40"
						/></a
					>
				</li>
			</ul>
		</div>
	</nav>
</main>

<style>
	@import url('https://fonts.googleapis.com/css2?family=Inter:wght@400;700&display=swap');

	.container {
		max-width: 1400px;
		margin-left: 50px;
		margin-right: 50px;
		display: flex;
		justify-content: space-between;
		align-items: center;
	}
	a:hover {
		transition: all 0.3s ease;
		transform: scale(1.2);
		color: #ff748d;
	}

	.navbar-brand img {
		width: 70px;
	}

	.navbar-nav {
		display: flex;
		list-style: none;
		margin: 0;
		padding: 0;
	}

	.nav-item {
		margin-left: 20px;
		font-family: 'Inter', sans-serif;
		font-weight: 700;
		font-size: 30px;
	}

	a {
		display: block;
		padding: 10px;
		color: #2f2f2f;
		text-decoration: none;
		transition: all 0.3s ease;
		transform: scale(1);
		color: #2f2f2f;
	}

	.git {
		margin-top: 2px;
	}

	@media screen and (max-width: 600px){
		*{
			margin: 0;
			padding: 0;
			box-sizing: border-box;
		}

		a{
			font-size: 40px;
		}

		.container{
			flex-direction: column;
			margin-left: 0;
			margin-right: 0;
			min-width: 700px;
			padding-top: 50px;
		}


	} 
</style>
