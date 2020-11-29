<script>
	export let name;
	import Comp from "./Comp.svelte";
	import CarbonBtn from "./CarbonBtn.svelte";
	import CarbonTable from "./CarbonTable.svelte";
	import Apitest from "./Apitest.svelte";
</script>

<style>
	main {
		text-align: center;
		padding: 1em;
		max-width: 240px;
		margin: 0 auto;
		background-color: rgb(37, 37, 37);
	}

	h1 {
		color: #ff3e00;
		text-transform: uppercase;
		font-size: 4em;
		font-weight: 100;
	}

	@media (min-width: 640px) {
		main {
			max-width: none;
		}
	}
</style>

<main>
	<h1>Hello {name}!</h1>
	<p>
		Visit the
		<a href="https://svelte.dev/tutorial">Svelte tutorial</a>
		to learn how to build Svelte apps.
	</p>
	<Comp pr="test" />
	<Comp />
	<CarbonBtn name="testname" kind="danger" size="small" />
	<CarbonTable />
	<Apitest />
</main>
