<svelte:head>
	<title>About</title>
</svelte:head>




<style>
	.about {
			background-color: #FFBD2A;
			width: 100%;
			height: 100vh;
			text-align: center;
		}

		h4 {
			margin: 0;
			font-size: 40px;
		}

		p {
			font-size: 20px;
		}

		p li {
			list-style: disc;
		}

		h4, p {
			position: relative;
			top: 10%;
		}
			

	a {
		text-decoration: none;
		color: #353535;
		font-weight: bold;
		font-size: 18px;
		transition: all 0.25s ease;
	}

	a:hover {
		color: #222;
		text-shadow: 0px 2px 2px #353535;
	}
</style>


<section class="about">
	<h4>Acerca</h4>
	<p>Esta es una pagina web para practicar, <br>
		 no es un negocio real ni nada por el estilo. <br>
		 Creado por <a href="https://github.com/SantiagoVA" target=_blank > Santiago Vasquez Arboleda</a> <br>
	Tecnologias usadas: <br>
<li>Svelte</li>
<li>Sapper</li>
<li>Firebase</li>
</p>
</section>
