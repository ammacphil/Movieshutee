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

<style>
    .popular__movies{
        display: grid;
        grid-template-columns:repeat(auto-fit, minmax(15.625rem, 1fr)) ;
        grid-column-gap:0.25rem ;
        grid-row-gap: 1.2rem;
    }
    
</style>