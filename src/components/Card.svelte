<script>
    export let movie;
</script>

<div class="movie">
    <img src={'https://image.tmdb.org/t/p/w500' + movie.poster_path} alt={movie.title} />
</div>
<div class="descr">
    <h2>{movie.title}</h2>
    <p>{movie.release_date}</p>
    <p>{movie.vote_average}</p>
</div>