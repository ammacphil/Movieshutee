<script context="module">
	export async function load({ fetch }) {
		//fetch data
		const res = await fetch(`https://api.themoviedb.org/3/movie/popular?api_key=58791a9d5f40e2836e8f1c41d2f01222&language=en-US&page=1`);
		//get the fetch json data
		const data = await res.json();
        console.log(data)
		if (res.ok) {
			//return the fetched result
			return {
				props: { popular: data.results }
			};
		}
	}
</script>

<script>
    import PopularMovies from "../components/PopularMovies.svelte";
    export let popular;
    //console.log(popular);
</script>


<section>
    <PopularMovies {popular}/>

</section>