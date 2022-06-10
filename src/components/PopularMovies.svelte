<script>
	export let popular;
	//console.log(popular)
	import Card from './Card.svelte';
</script>

<h3>Popular Movies</h3>

<section class="popular__movies">
	<!--{#each}{/each} => forEach function-->
	{#each popular as movie}
		<Card  {movie}/>
	{/each}
</section>
