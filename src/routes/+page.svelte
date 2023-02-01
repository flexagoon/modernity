<script lang="ts">
	import ModernityButton from '$lib/components/ModernityButton.svelte';

	let date: Date = new Date();
	let year: number = date.getFullYear();
</script>

<div>
	<h1>Modernity</h1>
	<h2>"Because it's already {year}"</h2>
	<p>
		I believe that creating the technology of the future requires us to get rid of the technology of
		the past. The goal of Modernity is to encourage people to use modern standards and explain their
		clear benefits over outdated, legacy solutions.
	</p>
	<hr />
	<div id="projects">
		<ModernityButton
			title="Modernity check-lists"
			subtitle="Check how modern your systems are"
			href="/checklists"
		/>
		<p class="coming-soon">More projects coming soon...</p>
	</div>
</div>

<style lang="scss">
	h1 {
		margin-top: 150px;
		margin-bottom: 0px;
	}

	h2 {
		margin-top: 0px;
	}

	p {
		margin-top: 25px;
		margin-bottom: 25px;
	}

	#projects {
		text-align: left;
	}

	.coming-soon {
		font-size: 36px;
		font-weight: 300;
		margin-top: 50px;
	}
</style>
