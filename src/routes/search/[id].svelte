<script context="module">
	export async function load({ fetch, params }) {
		//fetch data
		const res = await fetch(
            `https://api.themoviedb.org/3/search/movie?api_key=58791a9d5f40e2836e8f1c41d2f01222&language=en-US&query=${params.id}&page=1&include_adult=false`
		);
		//get the fetch movieDetails json data
		const data = await res.json();
		if (res.ok) {
            //console.log(data)
			//return the fetched result
			return {
				props: { searchedMovie: data.results }
			};
		}
	}
</script>

<script>
	import Card from '../../components/Card.svelte';
    export let searchedMovie;
</script>


<div class="movies__searched">
    {#each searchedMovie as movie}<Card {movie} /> {/each}
</div>

<style>
    .movies__searched{
        display: grid;
        grid-template-columns:repeat(auto-fit, minmax(15.625rem, 1fr)) ;
        grid-column-gap:0.25rem ;
        grid-row-gap: 1.2rem;
        height: 20vh;
    }
</style>



