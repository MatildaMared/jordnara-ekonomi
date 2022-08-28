<script lang="ts">
	import Heading from "$lib/heading/Heading.svelte";
</script>

<section class="about">
	<Heading>
		Om mig
	</Heading>
	<div class="content">
		<img src="images/jan-erik3.jpg" alt="Jan-Erik Mattsson" class="photo">
		<div>
			<p>
				Mitt namn är Jan-Erik Matsson. Jag är specialist inom jord- och skogsbruk och har lång erfarenhet av
				redovisning i många olika branscher.
			</p>
			<p>
				Jag tittar på er befintliga organisation och ger förslag utifrån vad som skulle passa er bäst.
			</p>

			<p><strong>Jag har..</strong></p>
			<ul>
				<li>
					högskoleutbildning inom ekonomi
				</li>
				<li>
					mångårig erfarenhet av jord- och skogsbruk
				</li>
				<li>
					lång erfarenhet av EU-bidrag till jord-och skogsbruk
				</li>
			</ul>
		</div>
	</div>
</section>

<style lang="scss">
	@use "../../styles/breakpoints" as *;

	.about {
		margin: var(--spacing-xl) 0;
		display: flex;
		flex-direction: column;
		align-items: center;
		padding: 0 16px;
	}

	.content {
		display: flex;
		flex-direction: column;
		align-items: center;
		width: 100%;
		gap: 32px;
		max-width: 800px;

		@media (min-width: $breakpoint-tablet-portrait) {
			flex-direction: row;
		}

		p {
			margin-bottom: var(--spacing-xs);
		}

		.photo {
			width: 100%;
			max-width: 350px;
			height: auto;
			max-height: 350px;
			border-radius: 50%;
			aspect-ratio: 1/1;
			object-fit: cover;
			object-position: 0 -100px;
			border: 1px solid hsla(131, 20%, 28%, .75);
		}

		ul {
			padding: 0 16px;
			width: fit-content;
			margin: 0 auto;

			li {
				margin-bottom: var(--spacing-xs);
			}
		}
	}
</style>