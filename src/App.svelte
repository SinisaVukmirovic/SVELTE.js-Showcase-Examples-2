<script>
	import Header from './Header.svelte';
	import Numeric from './Numeric.svelte';
	import Checkcontinue from './Checkcontinue.svelte';
	import Groupinput from './Groupinput.svelte';
	import Todos from './Todos.svelte';
	import Dimensions from './Dimensions.svelte';
	import Progressbar from './Progressbar.svelte';
	import Footer from './Footer.svelte';
</script>

<style>
	.container {
		font-size: 1.25rem;
		width: 60%;
		margin: 1em auto;
		padding: 1em;
	}

	@media screen and (max-width: 900px) {
		.container {
			width: 80%;
		}
	}

	@media screen and (max-width: 768px) {
		.container {
			width: 90%;
		}
	}
</style>

<Header></Header>

<div class="container">

	<h3>Ranges Sum</h3>
	<Numeric></Numeric>

	<hr>

	<h3>Want to learn more about Svelte.js?</h3>
	<Checkcontinue></Checkcontinue>

	<hr>

	<Groupinput></Groupinput>

	<hr>

	<h3>ToDos</h3>
	<Todos></Todos>

	<hr>

	<Dimensions></Dimensions>

	<hr>

	<h3>Rate your progress with SVELTE.js</h3>
	<Progressbar></Progressbar>

</div>

<Footer></Footer>