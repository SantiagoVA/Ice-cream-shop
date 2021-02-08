<script>
	import { onMount } from 'svelte';
	import { fly } from 'svelte/transition';
	

	let ready = false;
  onMount(() => ready = true);
</script>

<section class="main">

{#if ready}
<h1 in:fly="{{duration: 1000, y: 70, delay: 200}}">Cream <br>
	Cream!</h1>

	
	
	<div class="images">
		
	<img in:fly="{{duration: 1000, x: 70, delay: 500}}" class="products-image"src="assets/detalles-producto.png" alt="Detalles producto">
	<img in:fly="{{duration: 1000, x: 70, delay: 1000}}" class="products-image-2"  src="assets/back-product.png" alt="Detalles producto">
	
</div>
{/if}
</section>
<div class="father-section2">
<section class="section2">
	<h2>Productos</h2>

	
	<div class="products">
		
		<div class="card">
			<img class="img-product" src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcSb_O66gCaX7DzViGzoAe3Ya3hXCs6KgWdjzQ&usqp=CAU" alt="">
			<div class="card-text">
				<h3>Nombre helado</h3>
			<p>Descripcion helado</p>
			<button><a class="checkout" href="/checkout">Comprar</a> </button>
			</div>
		
		</div>
	</div>
</section>
</div>

<style>
	.main {
		background-color: #FFBD2A;
		width: 100%;
		height: 100vh;
	}

	.products {
		display: flex;
		justify-content: center;
		position: relative;
		top: 5%;
	}

	button a {
		text-decoration: none;
		color: #353535;
	}

	button {
		background-color: #FFBD2A;
		color: #353535;
		font-weight: bold;
		font-size: 20px;
		border: none;
		border-radius: 10px;
		margin-top: 30px;
		transition: all 0.25s ease;
		cursor: pointer;
	}

	button:hover {
		background-color: #bfff2a;
	}

	h1 {
		color: #353535;
		font-size: 110px;
		position: relative;
		margin: 0;
		left: 20px;
		top: 20%;
	}

	.images {
		position: absolute;
		top: 4.7%;
		left: 59.7%;
	}

	.products-image {
		position: absolute;
		width: 500px;
		z-index: 2;
	}

	.products-image-2 {
		position: absolute;
		width: 350px;
		top: 79px;
		left: 200px;
		z-index: 1;
	}

	.section2 {
		width: 100%;
		height: 100vh;
		z-index: -2;
	}

	.father-section2 {
		background-size: cover;
		background-color: transparent;
		background-image: url("data:image/svg+xml,%3Csvg width='600' height='120' viewBox='0 0 100 20' xmlns='http://www.w3.org/2000/svg'%3E%3Cpath d='M21.184 20c.357-.13.72-.264 1.088-.402l1.768-.661C33.64 15.347 39.647 14 50 14c10.271 0 15.362 1.222 24.629 4.928.955.383 1.869.74 2.75 1.072h6.225c-2.51-.73-5.139-1.691-8.233-2.928C65.888 13.278 60.562 12 50 12c-10.626 0-16.855 1.397-26.66 5.063l-1.767.662c-2.475.923-4.66 1.674-6.724 2.275h6.335zm0-20C13.258 2.892 8.077 4 0 4V2c5.744 0 9.951-.574 14.85-2h6.334zM77.38 0C85.239 2.966 90.502 4 100 4V2c-6.842 0-11.386-.542-16.396-2h-6.225zM0 14c8.44 0 13.718-1.21 22.272-4.402l1.768-.661C33.64 5.347 39.647 4 50 4c10.271 0 15.362 1.222 24.629 4.928C84.112 12.722 89.438 14 100 14v-2c-10.271 0-15.362-1.222-24.629-4.928C65.888 3.278 60.562 2 50 2 39.374 2 33.145 3.397 23.34 7.063l-1.767.662C13.223 10.84 8.163 12 0 12v2z' fill='%23ffbd2a' fill-opacity='1' fill-rule='evenodd'/%3E%3C/svg%3E");

	}

	h2 {
		margin: 0;
		text-align: center;
		font-size: 40px;
	}

	

		.card {
			width: 250px;
			height: 400px;
			background-color: white;
			z-index: 2;
			border-radius: 10px;
			box-shadow: 3px 4px 4px 1px rgba(67, 67, 67, 0.638);
			text-align: center;
		}

		.img-product {
			width: 250px;
			border-top-right-radius: 10px;
			border-top-left-radius: 10px;
		}

		

		@keyframes breathEffect {
			0% {
				width: 40%;
				height: 80vh;
			}

			50%{
				width: 41%;
				height: 81vh;
			}

			100% {
				width: 40%;
				height: 80vh;
			}
		}


	@media (max-width: 829px){
		.images {
			display: none;
		}

		h1 {
			position: relative;
			padding: 0;
			text-align: center;
		}
	}

	@media (max-width: 640px){
		h1 {
			font-size: 80px;
		}

		.images {
			text-align: center;
		}

		.products-image-2, .products-image {
			position: relative;
			top: auto;
			left: auto;
		}
		

		
	}
</style>