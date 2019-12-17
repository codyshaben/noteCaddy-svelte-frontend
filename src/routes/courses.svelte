<script>

    import { onMount } from 'svelte'

        let results = []

        onMount (async () => {
            const response = await fetch('https://polar-temple-23743.herokuapp.com/api/v1/courses')
			results = await response.json()
			results.forEach(result => {
				results.push(result)
			});
		})

</script>

<style>
@import url('https://fonts.googleapis.com/css?family=Saira+Extra+Condensed&display=swap');

.course-list {
	list-style-type: none;
	padding: 2rem;
	display: flex;
	flex-direction: row;
	flex-wrap: wrap;
	justify-content: center;
	margin-top: 0rem;
}

.course {
	font-family: 'Saira Extra Condensed', sans-serif;
	list-style-type: none;
	background-color: rgb(247, 244, 244);
	margin-top: 1rem;
	border-radius: .25rem;
	padding: 1rem;
	width: 25rem;
	margin: 1rem;
}


h1 {
	font-family: 'Saira Extra Condensed', sans-serif;
	color: #05386B;
	padding: 1rem;
	text-align: center;
	background-color: #8EE4AF
}

h2 {
	margin-bottom: 0rem;
	border-left: solid;
	padding-left: .25rem
}

h3 {
	font-family: 'Saira Extra Condensed', sans-serif;
	color: #05386B;
	padding: 0rem;
	text-align: center;	
}

.course-header {
	display: flex;
	flex-direction: row;
	justify-content: space-between;
	align-items: center
}

.name-location {
	vertical-align: middle;
	font-family: 'Saira Extra Condensed', sans-serif;
	color: #05386B;
}

#course-location {
	margin-top: 0rem;
	border-left: solid;
	padding-left: .25rem;
	margin-bottom: 0rem
}

#course-image {
	width: 300px;
    height: 150px;
    margin-bottom: 20px;
	align-content: center
}

#add-course {
	font-family: 'Saira Extra Condensed', sans-serif;
	color: #05386B;
	font-size: 3rem;
	align-self: center;
	cursor: pointer;
	border: none;
	background-color: inherit;
}


@media (min-width: 480px) {
	#course-image {
		width: 400px;
		height: 200px
	}
}

</style>

<svelte:head>
	<title>About</title>
</svelte:head>

<h1 class='page-title'>Colorado Golf Courses</h1>

<h3>Add courses to your noteBook!</h3>

<ul class="course-list">
	{#each results as result}
	<li class="course"> 
		<div class="course-header">
			<section class='name-location'>
				<h2>{result.name}</h2>
				<p id='course-location'>{result.location}, CO</p>
			</section>
			<aside>
				<button id="add-course">+</button>
			</aside>
		</div>
		<img src={result.image} alt="Not Found" onerror='this.src="https://dubsism.files.wordpress.com/2017/12/image-not-found.png?w=1094"' id="course-image">
	</li>
	{/each}
</ul>