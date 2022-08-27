<script lang="ts">
	import Link from "$lib/link/Link.svelte";
</script>

<header>
	<h1 class="title">Jordnära ekonomi</h1>
	<p class="subtitle">Redovisning med fötterna på jorden</p>
	<Link url="#vad-vi-erbjuder" primary>Så kan vi hjälpa dig</Link>
</header>

<style lang="scss">
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

		.title {
			font-size: 4.5rem;
			text-shadow: 0 4px 8px hsla(131, 20%, 8%, .5);
		}

		.subtitle {
			font-family: var(--font-script);
			font-size: 2rem;
			text-shadow: 0 3px 6px hsla(131, 20%, 8%, .3);
		}
	}
</style>