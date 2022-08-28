<script lang="ts">
	export let url;
	export let secondary = false;
</script>

<a href={url} class={secondary ? "secondary link" : "link"}>
	<slot/>
</a>

<style lang="scss">
	.link {
		background-color: var(--color-primary-dark);
		padding: 16px 32px;
		border-radius: 8px;
		color: rgba(255, 255, 255, 0.95);
		text-decoration: none;
		margin: 32px 0;
		box-shadow: 0 4px 8px rgba(0, 0, 0, .5);
		transition: all .2s;

		&.secondary {
			background-color: var(--color-secondary-dark);
		}

		&:hover {
			transform: translateY(-2px);
			box-shadow: 0 8px 16px rgba(0, 0, 0, .5);
			background-color: var(--color-primary);
			color: rgba(255, 255, 255, 0.95);

			&.secondary {
				background-color: var(--color-secondary);
			}
		}

		&:active {
			transform: translateY(-1px);
		}
	}
</style>