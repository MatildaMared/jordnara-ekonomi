<script lang="ts">
	import Link from "$lib/link/Link.svelte";
</script>

<header>
	<h1 class="title">Jordnära ekonomi</h1>
	<p class="subtitle">Redovisning med fötterna på jorden</p>
	<Link url="#tjanster" secondary>Så kan jag hjälpa dig</Link>
</header>

<style lang="scss">
	@use "../../styles/breakpoints" as *;

	header {
		background: linear-gradient(
						rgba(0, 0, 0, 0.15),
						rgba(0, 0, 0, 0.25)
		), url("/images/skog.jpg") no-repeat center;
		background-size: cover;
		height: 100%;
		min-height: 80vh;
		display: flex;
		flex-direction: column;
		justify-content: center;
		align-items: center;
		color: rgba(255, 255, 255, .9);
		text-align: center;
		line-height: 1.2;
		padding: 0 16px;

		.title {
			font-size: 2.5rem;
			text-shadow: 0 4px 8px hsla(131, 20%, 8%, .5);
		}

		.subtitle {
			font-family: var(--font-script);
			font-size: 1.2rem;
			text-shadow: 0 3px 6px hsla(131, 20%, 8%, .3);
		}

		@media (min-width: $breakpoint-tablet-portrait) {
			.title {
				font-size: 3.5rem;
			}
			.subtitle {
				font-size: 1.6rem;
			}
		}

		@media (min-width: $breakpoint-tablet-landscape) {
			.title {
				font-size: 4.5rem;
			}
			.subtitle {
				font-size: 2rem;
			}
		}
	}
</style>