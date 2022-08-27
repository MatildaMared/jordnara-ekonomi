<script lang="ts">
	const API_KEY = "AIzaSyB32uPsHhFH6LILWZraOjY_irVKz_NyhOg";
</script>

<section class="contact">
	<h1>Kontakt</h1>
	<iframe
			class="map"
			loading="lazy"
			allowfullscreen
			referrerpolicy="no-referrer-when-downgrade"
			src={`https://www.google.com/maps/embed/v1/place?key=${API_KEY}&zoom=10&maptype=satellite&q=Mossarp+406+313+93+Slättåkra`}>
	</iframe>
</section>


<style lang="scss">
	.contact {
		width: 100%;
		max-width: var(--max-width);
	}

	.map {
		border: 1px solid hsla(131, 20%, 18%, .95);
		width: 100%;
		height: 300px;
	}
</style>