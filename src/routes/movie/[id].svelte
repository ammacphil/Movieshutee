<script context="module">
	export async function load({ fetch, params }) {
		//fetch data
		const res = await fetch(
			`https://api.themoviedb.org/3/movie/${params.id}?api_key=58791a9d5f40e2836e8f1c41d2f01222&language=en-US`
		);
		//get the fetch movieDetails json data
		const movieDetails = await res.json();
		if (res.ok) {
			//return the fetched result
			return {
				props: { movieDetails }
			};
		}
	}
</script>

<script>
	export let movieDetails;
    console.log(movieDetails)
</script>

<div class="movie__details__sect">
	<div class="container">
		<img
			src={'https://image.tmdb.org/t/p/original' + movieDetails.backdrop_path}
			alt={movieDetails.title}
		/>
	</div>
    <div class="descr">
        <span><h2>{movieDetails.original_title}</h2></span>
        <span><h3>Watch Time:{movieDetails.runtime} minutes</h3></span>
        <span><h4>Released Date:{movieDetails.release_date}</h4></span>
        <span><p>{movieDetails.overview}</p></span>
        <span><p>Box Office Budget:{movieDetails.budget}$</p></span>
        <span><p>Film Revenue:{movieDetails.revenue}$</p></span>
    </div>
</div>

<style>
    .movie__details__sect{
        width: 100%;
        display: flex;
    }
    .container{
        width: 1000px;
    }
    img{
        width: 100%;
        object-fit: contain;
    }
</style>
