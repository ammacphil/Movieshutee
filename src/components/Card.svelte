<script>
	export let movie;
</script>

<div class="movie">
	<a href={'/movie/' + movie.id}>
		<img src={'https://image.tmdb.org/t/p/w500' + movie.poster_path} alt={movie.title} />
	</a>
	<div class="descr">
		<h4>{movie.title}</h4>
		<span class="details">
			<p>Release: {movie.release_date}</p>
			<p>Rating: {movie.vote_average}</p>
		</span>
	</div>
</div>

<style>
	img {
		width: 100%;
		object-fit: contain;
		margin-bottom: 1rem;
	}
	.movie {
		cursor: pointer;
		display: flex;
		flex-direction: column;
		padding: 00.75rem;
		justify-content: space-around;
	}
	.descr {
		/*background-color: red;*/
		height: 10vh;
	}
	.details {
		width: 100%;
		display: flex;
		gap: 20px;
	}
	p {
		font-size: 0.75rem;
	}
</style>
