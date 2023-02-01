<script lang="ts">
	export let title: string;
	export let subtitle: string | undefined = undefined;
	export let href: string;
</script>

<a {href}>
	<p class="title">{title} -></p>
	{#if subtitle} <p class="subtitle">{subtitle}</p> {/if}
</a>

<style lang="scss">
	a {
		color: black;
		text-decoration: none;
		text-align: left;
	}

	p {
		margin: 0px;
	}

	.title {
		font-size: 48px;
		font-weight: 500;
	}

	.subtitle {
		font-size: 24px;
		font-weight: 300;
	}
</style>
