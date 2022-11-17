<script>
	import { onMount } from 'svelte';
	
	export let inputUrl;

	let textarea;
	
	onMount(() => {
		textarea.select();
		document.execCommand('copy');
	});
</script>

<textarea bind:value={inputUrl} bind:this={textarea}></textarea>
