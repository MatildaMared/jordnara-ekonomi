<script lang="ts">
	import {MailIcon, MapPinIcon, PhoneIcon} from "svelte-feather-icons";

	const API_KEY = "AIzaSyB32uPsHhFH6LILWZraOjY_irVKz_NyhOg";
</script>

<section class="contact">
	<h1>Kontakt</h1>
	<div class="contact_group">
		<PhoneIcon/>
		<div>
			<h3>Telefon</h3>
			<a href="tel:070-3369170">070-3369170</a>
		</div>
	</div>
	<div class="contact_group">
		<MailIcon/>
		<div>
			<h3>E-post</h3>
			<a href="mailto:jordnaraekonomi@outlook.com">jordnaraekonomi@outlook.com</a>
		</div>
	</div>
	<div class="contact_group">
		<MapPinIcon/>
		<div>
			<h3>Adress</h3>
			<p>Mossarp 406, 313 93 Slättåkra</p>
		</div>
	</div>
	<iframe
			title="Google Maps"
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
		display: flex;
		flex-direction: column;
		align-items: center;
		padding: var(--spacing-xl) 0;
		background-color: var(--color-primary-dark);

		> * {
			max-width: var(--max-width);
		}

		&_group {
			border: 1px solid red;
			margin-bottom: var(--spacing-s);
			display: flex;
			align-items: center;

			& > div {
				margin-left: 8px;
			}
		}
	}

	.map {
		border: 1px solid hsla(131, 20%, 22%, .95);
		width: 100%;
		height: 300px;
	}
</style>