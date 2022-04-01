<script context="module">
	export const load = async () => {
		const HomePage = await import('../../index.md');
		const Home = HomePage.default;

		return {
			props: {
				Home
			}
		};
	};
</script>

<script>
	export let Home;
</script>

<svelte:head>
	<title>6 Pak's Site</title>
</svelte:head>

<svelte:component this={Home} />
