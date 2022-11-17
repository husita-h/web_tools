<script>
    let result;

    async function testFunc1(){
        // https://scottspence.com/posts/sveltekit-environment-variables-with-the-sveltekit-env-module
        // const url = import.meta.env.MOCK_API_ENDPOINT;
        const url = import.meta.env.VITE_MOCK_API_ENDPOINT;
        // const url = process.env['MOCK_API_ENDPOINT']
        const response = await fetch(url, { mode: "no-cors" })
        console.log(url);
        console.log(response);
        result = response;
        return;
    }
    function clear(){
        result = null;
        return;
    }
</script>

<h1>Post Issues</h1>

<button on:click={testFunc1}>testFunc1</button>
<button on:click={clear}>clear</button>

<div>result: {result || ""}</div>