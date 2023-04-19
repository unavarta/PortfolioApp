<script>
	import Circles from '../assets/circles.svg';
</script>

<main>
	<img src={Circles} alt="" />
</main>

<style>
	img {
		margin-left: 50px;
		margin-top: 30px;
		position: fixed;
		bottom: 60px;
	}

	@media screen and (max-width: 600px) {
		img {
			
			bottom: 20px;
		}
		main{
			min-width: 600px;
			display: flex;
			justify-content: center;
			align-items: center;
			margin: 0 auto;
		}
	}
</style>
