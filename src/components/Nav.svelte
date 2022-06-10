<nav>
	<div class="container">
		<div class="logo">
			<h3><a href="/">🎬movieshutee</a></h3>
		</div>
		<div class="search">
			<span class="home"><a href="/">Home</a></span>
			<span class="search__input">
				<input type="text" placeholder="search movie" />
			</span>
		</div>
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
	.search {
		width: 60%;
		display: flex;
		gap: 1.875rem;
		align-items: center;
	}
	.home a {
		cursor: pointer;
		border-bottom: 2px solid hsl(222, 53%, 14%);
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
		.container {
			display: flex;
			flex-direction: column;
            width: 100%;
            padding: 10px 0;
            height: 120px;
            align-items: flex-start;
            margin-bottom: 2%;
		}
        .logo{
            width:100%;
        }
        .logo h3 a{
            font-size: 16px;
            font-family:'Nunito', 'Catamaran', 'Dancing Script', sans-serif, cursive;
            letter-spacing: 0.156rem;
        }
        .home a{
            display: none;
        }
        .search{
            display: flex;
            align-items: center;
            justify-content: center;
            width: 100%;
            height: 100%;
            margin-top: 5%;
        }
	}
</style>
