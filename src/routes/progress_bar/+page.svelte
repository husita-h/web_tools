<script>
	import { writable } from 'svelte/store';

	const progress = writable(0);
</script>

<h1>Progress Bar</h1>

<progress value={$progress}></progress>

<button on:click="{() => progress.set(0)}">
	0%
</button>

<button on:click="{() => progress.set(0.25)}">
	25%
</button>

<button on:click="{() => progress.set(0.5)}">
	50%
</button>

<button on:click="{() => progress.set(0.75)}">
	75%
</button>

<button on:click="{() => progress.set(1)}">
	100%
</button>

<p>Back <a href="http://localhost:5173/">link</a> to Top Page</p>

<style>
	progress {
		display: block;
		width: 100%;
	}
</style>