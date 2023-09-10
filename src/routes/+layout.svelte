<script>
	import Header from './Header.svelte'
	import Footer from './Footer.svelte'
</script>
<div class="app">
	<Header />
	<main>
		<slot />
	</main>
	<Footer />
</div>

<style>
	section {
		margin-right: 10vw;
		margin-bottom: 4.5em;
	}
</style>
