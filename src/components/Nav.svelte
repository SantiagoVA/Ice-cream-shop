<script>
	export let segment;
</script>

<style>
	nav {
		width: 100%;
		position: absolute;
		z-index: 100;
		font-weight: 300;
		padding: 0;
		padding-left: 20px;
	}

	ul {
		width: 100%;
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


	[aria-current]::after {
		position: absolute;
		content: '';
		width: calc(100% - 99.2%);
		height: 3px;
		background-color: #353535;
		display: block;
		bottom: 25px;
		transition: all 0.25s ease;
	}

	[aria-current]:hover::after {
		background-color: #222;
		width: calc(100% - 95.8%);
	}



	a {
		color: #353535;
		font-weight: bold;
		font-size: 18px;
		text-decoration: none;
		padding: 1em 10%;
		display: block;
		transition: all 0.25s ease;
		
	}

	a:hover {
		color: #222;
	}

	

	.logo-img{
		width: 30%;
	}


	

</style>

<nav>
	<div class="container-nav">
	<ul>
		<li><a href="."><img class="logo-img" src="../assets/logo.png" alt="logo"></a></li>
		<li class="push-right"><a class="about-nav" aria-current="{segment === 'about' ? 'page' : undefined}" href="about">Acerca</a></li>
	</ul>
</div>
</nav>


