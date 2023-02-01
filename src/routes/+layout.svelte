<script lang="ts">
	import '$lib/scss/main.scss';
</script>

<div>
	<slot />
</div>

<style>
	div {
		margin-left: auto;
		margin-right: auto;
		padding-left: 10px;
		padding-right: 10px;
		max-width: 775px;
	}
</style>
