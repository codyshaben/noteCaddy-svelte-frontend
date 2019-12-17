<script>
	export let segment;
</script>

<style>
	nav {
		border-bottom: 1px solid #8EE4AF; 
		font-weight: 300;
		padding: 0 1em;
		color: #05386B;
		background-color: #EDF5E1;
	}

	ul {
		margin: 0;
		padding: 0;
	}

	/* clearfix */
	ul::after {
		content: '';
		display: block;
		clear: both;
	}

	li {
		display: block;
		float: left;
	}

	.selected {
		position: relative;
		display: inline-block;
	}

	.selected::after {
		position: absolute;
		content: '';
		width: calc(100% - 1em);
		height: 2px;
		background-color:#05386B;
		display: block;
		bottom: -1px;
	}

	a {
		text-decoration: none;
		padding: 1em 0.5em;
		display: block;
	}
</style>

<nav>
	<ul>
		<li><a class:selected='{segment === undefined}' href='.'>home</a></li>
		<li><a class:selected='{segment === "courses"}' href='courses'>courses</a></li>

		<!-- for the blog link, we're using rel=prefetch so that Sapper prefetches
		     the blog data when we hover over the link or tap it on a touchscreen -->
		<li><a rel=prefetch class:selected='{segment === "noteBook"}' href='noteBook'>noteBook</a></li>
		<li><a rel=prefetch class:selected='{segment === "signup"}' href='signup'>sign up</a></li>
	</ul>
</nav>
