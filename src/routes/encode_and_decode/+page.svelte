<script>
  import CopyClipBoard from '../../lib/components/CopyClipBoard.svelte';

	let inputUrl = "";
	let result = "";

  function decode(url){
    result = decodeURI(url);
  }

	const copy = () => {
		const app = new CopyClipBoard({
			target: document.getElementById('clipboard'),
			props: { inputUrl },
		});
		app.$destroy();
	}
</script>

<h1>URL decode</h1>
<div>
  <div>
    <input bind:value={inputUrl} placeholder="Input URL">
    <button on:click={decode(inputUrl)}>run</button>
    <div>input: {inputUrl}</div>
  </div>
  
  <div>
    <input bind:value={result}>
    <button on:click={copy}>copy</button>
    <div>output: {result}</div>
    <div id="clipboard"></div>
  </div>
</div>
