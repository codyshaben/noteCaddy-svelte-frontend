<script>
	// export let segment;
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

.signup-container {
    align-content: center;
    background-color: #8EE4AF;
    color: #05386B;
	padding: 1rem;
	border-radius: .25rem;
	align-self: center;
	width: 50%;
	font-family: 'Saira Extra Condensed', sans-serif;
	max-width: 20rem;
	opacity: .75;
}

#welcome-page {
	display: flex;
	justify-content: center;
	flex-direction: column;
	padding-bottom: 10rem
}

#signup-form {
	display: flex;
	flex-direction: column;
	font-family: 'Saira Extra Condensed', sans-serif;
	padding: 2rem;

}

.signup-input {
	font-family: 'Saira Extra Condensed', sans-serif;
	padding: .15rem;
	font-size: .8rem;
	border-radius: .25rem;
	margin-top: .25rem;
	color: #05386B

}

.button {
	font-family: 'Saira Extra Condensed', sans-serif;
	font-size: .8rem;
	padding: .15rem;
	border-radius: .25rem;
	margin-top: 1rem;
}

.button:hover {
	cursor: pointer;
}


	@media (min-width: 480px) {
		h1 {
			text-align: center;
			align-self: center;
			font-size: 4em;
		}

		#signup-form {
			text-align: center;
		}

		.signup-container{
			width: 50%
		}

		.signup-input {
			padding: .4rem;
			font-size: 1.2rem;
		}

		.button {
			padding: .25rem;
			font-size: 1.2rem 
		}


	}
</style>


<div id="welcome-page">
	<h1>Welcome To noteCaddy</h1>

	<section class="signup-container">
		<form id="signup-form" method="post" name="signupForm">
			<input class="signup-input" type="text" name="username" placeholder="username"/>
			<input class="signup-input" type="password" name="password" placeholder="password"/>
            <input class="signup-input" type="password" name="password" placeholder="password confirmation"/>
			<input type="button" value="Sign Up" class="button" onclick="validate()"/>
		</form>
	</section>
</div>