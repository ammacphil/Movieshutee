<script>
	let inputMovies = '';
	import { goto } from '$app/navigation';
import Id from '../routes/search/[id].svelte';
import Nav from './Nav.svelte';

	function searchTheMovie() {
		goto('/search/' + inputMovies);
	}
</script>




<!--HTML Search-->
<div class="search">
	<span class="home"><a href="/">Home</a></span>
	<form on:submit|preventDefault={searchTheMovie} class="search__input">
		<input bind:value={inputMovies} type="text" placeholder="search movie" />
	</form>
</div>

<style>
	.search {
		width: 60%;
		display: flex;
		gap: 1.875rem;
		align-items: center;
	}
	.home a {
		cursor: pointer;
		border-bottom: 2px solid hsl(222, 53%, 14%);
		text-decoration: none;
	}
	input[type='text'] {
		padding: 5px;
		outline: none;
		border: 2px solid black;
		border-radius: 5px;
		color: black;
		font-family: 'Nunito', 'Catamaran', 'Dancing Script', sans-serif, cursive;
		font-weight: 600;
	}

	@media only screen and (max-width: 600px) {
		.home a {
			display: none;
		}
		.search {
			display: flex;
			align-items: center;
			justify-content: center;
			width: 100%;
			height: 100%;
			margin-top: 5%;
		}
	}
</style>
