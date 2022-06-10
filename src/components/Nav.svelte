<script>
	import Search from './Search.svelte';
</script>

<nav>
	<div class="container">
		<div class="logo">
			<h3><a href="/">🎬movieshutee</a></h3>
		</div>
		<Search />
	</div>
</nav>

<style>
	.container {
		/* background-color: rgb(255, 255, 255);*/
		width: 100%;
		padding: 1rem 0;
		display: flex;
		align-items: center;
	}
	.logo {
		width: 40%;
	}
	a {
		text-decoration: none;
		font-family: 'Dancing Script', sans-serif, cursive;
		font-size: 2rem;
		cursor: pointer;
		color: hsl(221, 69%, 43%);
	}
	

	@media only screen and (max-width: 600px) {
		.container {
			display: flex;
			flex-direction: column;
			width: 100%;
			padding: 10px 0;
			height: 120px;
			align-items: flex-start;
			margin-bottom: 2%;
		}
		.logo {
			width: 100%;
		}
		.logo h3 a {
			font-size: 16px;
			font-family: 'Nunito', 'Catamaran', 'Dancing Script', sans-serif, cursive;
			letter-spacing: 0.156rem;
		}
	}
</style>
