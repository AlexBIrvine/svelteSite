<script context="module">
	export const load = async () => {
		const ReadMeFile = await import('../../README.md');
		const ReadMe = ReadMeFile.default;

		return {
			props: {
				ReadMe
			}
		};
	};
</script>

<script>
	export let ReadMe;
</script>

<svelte:head>
	<title>6 Pak's Site</title>
</svelte:head>

<svelte:component this={ReadMe} />
