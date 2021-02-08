<script>
	import Nav from '../components/Nav.svelte';
	import Footer from '../components/Footer.svelte';
	export let segment;
</script>

<style>
	main {
		position: relative;
		background-color: white;
		padding: 0;
		margin: 0;
		box-sizing: border-box;
	}
</style>

<Nav {segment}/>

<main>
	<slot></slot>
</main>

<Footer/>