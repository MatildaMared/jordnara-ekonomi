<script lang="ts">
	import Heading from "$lib/heading/Heading.svelte";
	import Link from "$lib/link/Link.svelte";
</script>

<section class="offer" id="tjanster">
	<Heading>
		Tjänster
	</Heading>
	<div class="content">
		<img src="images/cows.jpg" alt="Cows on a field"/>
		<div>
			<article>
				<h3>Löpande redovisning</h3>
				<ul>
					<li>
						Redovisning av moms och arbetsgivaravgifter
					</li>
					<li>
						Löner
					</li>
					<li>
						Deklarationer
					</li>
					<li>
						Bokslut
					</li>
					<li>
						Årsredovisning för AB
					</li>
					<li>
						SAM ansökan
					</li>
					<li>
						Bilda ett AB
					</li>
					<li>
						Månadsvis rapportering om ditt företags ekonomiska status
					</li>
				</ul>
			</article>
			<article>
				<h3>Företagsekonomisk rådgivning</h3>
				<ul>
					<li>
						Är dina egna uttag eller lön anpassade till de skydd du behöver?
					</li>
					<li>
						Har du rätt företagsform?
					</li>
					<li>
						Är du rätt försäkrad?
					</li>
					<li>
						Får du ut optimalt av din SAM-ansökan?
					</li>
				</ul>
			</article>
		</div>
	</div>
	<p>Mina tjänster utnyttjas av olika typer av kunder, exempelvis hantverkare, konsulter, åkare, lantbrukare,
		mäklare, programmerare, maskinförare och musiker.
	</p>
	<p><strong>Kontakta mig så berättar jag mer!</strong></p>
	<Link url="#kontakt">Kontakt</Link>
</section>

<style lang="scss">
	@use "../../styles/breakpoints" as *;

	.offer {
		margin: var(--spacing-xl) 0 0 0;
		display: flex;
		flex-direction: column;
		align-items: center;
		padding: 0 16px;
	}

	p:not(:last-of-type) {
		text-align: center;
		max-width: 50ch;
		margin-bottom: var(--spacing-xs);
	}

	article:not(:last-of-type) {
		margin-bottom: var(--spacing-s);
	}

	h3 {
		text-transform: uppercase;
		color: var(--color-primary-dark);
		font-weight: 400;
		margin-bottom: 8px;
		font-size: 1.3rem;
		letter-spacing: 1px;
	}

	li:not(:last-of-type) {
		margin-bottom: 8px;
	}

	.content {
		display: flex;
		flex-direction: column;
		align-items: center;
		gap: 32px;
		margin-bottom: var(--spacing-m);

		@media (min-width: $breakpoint-tablet-portrait) {
			flex-direction: row;
			align-items: initial;
		}

		img {
			width: 100%;
			max-width: 400px;
			height: auto;
			border-radius: 8px;
			object-fit: cover;
		}
	}
</style>