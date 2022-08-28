<script lang="ts">
	export let light = false;
</script>

<h2 class={light ? "heading light" : "heading"}>
	<slot/>
</h2>

<style lang="scss">
	@use "../../styles/breakpoints" as *;

	.heading {
		margin-bottom: var(--spacing-m);
		font-size: 1.6rem;
		text-transform: uppercase;
		letter-spacing: 3px;
		font-weight: 400;
		position: relative;
		color: var(--color-primary-dark);
		width: fit-content;

		@media (min-width: $breakpoint-tablet-portrait) {
			font-size: 2rem;
		}

		&.light {
			color: rgba(255, 255, 255, .8);
		}

		&::before, &::after {
			content: "";
			width: 25%;
			height: 1px;
			background-color: var(--color-primary);
			position: absolute;
			opacity: .5;

			@media (min-width: $breakpoint-tablet-portrait) {
				width: 50%;
			}
		}

		&::before {
			top: 50%;
			left: calc(100% + 16px);
		}

		&::after {
			top: 50%;
			right: calc(100% + 16px);
		}
	}
</style>