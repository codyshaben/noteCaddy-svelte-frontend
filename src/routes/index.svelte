<script>
	export let segment;

</script>


<style>
@import url('https://fonts.googleapis.com/css?family=Saira+Extra+Condensed&display=swap');

h1 {
	font-family: 'Saira Extra Condensed', sans-serif;
	text-align: center;
	align-self: center;
	margin-bottom: 4rem;
	font-size: 3rem;
	margin-top: 2rem;
	color: #05386B
}

p {
	align-self: center;
	font-size: .8rem
}

.login-container {
    align-content: center;
    background-color: #8EE4AF;
    color: #05386B;
	padding: 1rem;
	border-radius: .25rem;
	align-self: center;
	width: 40%;
	font-family: 'Saira Extra Condensed', sans-serif;
	max-width: 20rem;
	opacity: .75;
}

.login-input {
	font-family: 'Saira Extra Condensed', sans-serif;
	padding: .15rem;
	font-size: .7rem;
	border-radius: .25rem;
	margin-top: .25rem;
	color: #05386B

}

.button {
	font-family: 'Saira Extra Condensed', sans-serif;
	font-size: .7rem;
	padding: .15rem;
	border-radius: .25rem;
	margin-top: 1rem;
}

.button:hover {
	cursor: pointer;
}

#welcome-page {
	display: flex;
	justify-content: center;
	flex-direction: column;
	padding-bottom: 10rem
}

#login-form {
	display: flex;
	flex-direction: column;
	font-family: 'Saira Extra Condensed', sans-serif;
	padding: 1.25rem;

}

#signup-link {
	text-decoration: inherit;
	font-size: 1.25rem;
	background-color: #EDF5E1;
	width: 40%;
	align-self: center;
	text-align: center;
	border-radius: .25rem
}

/* #logo {
	height: 15rem
} */


	@media (min-width: 480px) {
		h1 {
			text-align: center;
			align-self: center;
			font-size: 3.5em;
			margin: 1.5rem 0 3rem 0
		}

		#login-form {
			text-align: center;
			max-width: 20rem
		}

		.login-input {
			padding: .4rem;
			font-size: .9rem;
		}

		.button {
			padding: .25rem;
			font-size: .9rem 
		}

		#signup-link {
			font-size: 1.25rem;
		}


		p {
			font-size: 1rem
		}


	}
</style>

<svelte:head>
	<title>Sapper project template</title>
</svelte:head>

<div id="welcome-page">
	<header>
		<h1>Welcome To noteCaddy</h1>
	</header>

	<section class="login-container">
		<form id="login-form" method="post" name="loginForm">
			<input class="login-input" type="text" name="username" placeholder="username"/>
			<input class="login-input" type="password" name="password" placeholder="password"/>
			<input type="button" value="Login" class="button" onclick="validate()"/>
			<p>New to noteCaddy?</p>
			<a rel=prefetch class:selected='{segment === "signup"}' href='signup' id='signup-link'>Sign up! </a>
		</form>
		
	</section>
</div>


