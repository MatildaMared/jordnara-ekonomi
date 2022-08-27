<script lang="ts">
	import Header from "$lib/header/Header.svelte";
	import "../styles/reset.scss";
	import "../styles/variables.scss";
	import "../styles/globals.scss";
</script>

<Header/>

<main>
	<slot/>
</main>

<footer>

</footer>

<style lang="scss">
	main {
		display: flex;
		flex-direction: column;
		justify-content: center;
		align-items: center;
	}
</style>
