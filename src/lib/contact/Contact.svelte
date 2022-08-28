<script lang="ts">
	import {MailIcon, MapPinIcon, PhoneIcon} from "svelte-feather-icons";
	import Heading from "$lib/heading/Heading.svelte";

	const API_KEY = "AIzaSyB32uPsHhFH6LILWZraOjY_irVKz_NyhOg";
</script>

<section class="contact" id="kontakt">
	<Heading light>Kontakt</Heading>
	<div class="content_wrapper">
		<article class="contact__wrapper">
			<div class="contact__group">
				<div class="icon">
					<PhoneIcon size="32"/>
				</div>
				<div>
					<h3>Telefon</h3>
					<a href="tel:070-3369170">070-3369170</a>
				</div>
			</div>
			<div class="contact__group">
				<div class="icon">
					<MailIcon size="32"/>
				</div>
				<div>
					<h3>E-post</h3>
					<a href="mailto:jordnaraekonomi@outlook.com">jordnaraekonomi@outlook.com</a>
				</div>
			</div>
			<div class="contact__group">
				<div class="icon">
					<MapPinIcon size="32"/>
				</div>
				<div>
					<h3>Adress</h3>
					<p>Mossarp 406, 313 93 Slättåkra</p>
				</div>
			</div>
		</article>
		<iframe
				title="Google Maps"
				class="map"
				loading="lazy"
				allowfullscreen
				referrerpolicy="no-referrer-when-downgrade"
				src={`https://www.google.com/maps/embed/v1/place?key=${API_KEY}&zoom=10&maptype=satellite&q=Mossarp+406+313+93+Slättåkra`}>
		</iframe>
	</div>
</section>


<style lang="scss">
	@use "../../styles/breakpoints" as *;

	.contact {
		width: 100%;
		display: flex;
		flex-direction: column;
		align-items: center;
		padding: var(--spacing-xl) 16px;
		background-color: var(--color-primary-dark);

		> * {
			max-width: var(--max-width);
		}

		&__wrapper {
			background-color: rgba(255, 255, 255, .85);
			width: 100%;
			min-width: fit-content;
			padding: 32px;
			border-radius: 8px;
			border: 1px solid hsla(131, 20%, 22%, .95);
			height: 100%;
			flex: 1;
		}

		&__group {
			margin-bottom: 48px;
			display: flex;
			align-items: center;
			position: relative;

			&::after {
				opacity: .25;
				content: "";
				width: 75%;
				height: 1px;
				background-color: var(--color-primary-dark);
				position: absolute;
				top: calc(100% + 24px);
				left: 50%;
				transform: translateX(-50%);
			}

			&:last-of-type {
				margin-bottom: 0;

				&::after {
					display: none;
				}
			}

			& > div {
				margin-left: 16px;
			}

			h3, .icon {
				color: var(--color-primary-dark);
				text-transform: uppercase;
				font-weight: 300;
				letter-spacing: 1px;
			}
		}
	}

	.content_wrapper {
		width: 100%;
		display: flex;
		flex-direction: column;
		gap: 32px;

		@media (min-width: $breakpoint-tablet-portrait) {
			flex-direction: row;
		}
	}

	.map {
		flex: 2;
		border: 1px solid hsla(131, 20%, 22%, .95);
		width: 100%;
		min-height: 300px;
		max-height: 400px;
		border-radius: 8px;
	}

	a {
		color: var(--color-black);
		text-decoration: none;
		transition: all .2s;
		border-bottom: 1px solid transparent;

		&:hover {
			color: var(--color-primary-dark);
			border-bottom: 1px solid var(--color-primary-dark);
		}
	}
</style>