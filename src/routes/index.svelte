<script context="module">
  export const load = async () => {
		const ReadMeFile = await import('../../README.md');
    const ReadMe = ReadMeFile.default;

		return {
			props: {
				ReadMe
			}
		}
	}
</script>

<script>
  export let ReadMe
</script>


<svelte:head>
	<title>SvelteKit Static Blog Starter</title>
</svelte:head>


<svelte:component this={ReadMe} />
<!-- This is the README.md file in the root of the repo. It serves double duty as the homepage's content. If you'd rather use your own HTML and/or Svelte, you can delete/modify everything above this line. -->