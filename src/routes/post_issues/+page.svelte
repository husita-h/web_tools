<script>
    async function testFunc1(){
        const url = "http://localhost:9292/sub";
        const response = await fetch(url, { mode: "no-cors" })
        console.log(response)
        return response;
    }
    async function testFunc2(){
        const url = "https://status.cloud.google.com/incidents.json";
        const response = await fetch(url).then((response) => console.log(response));
        console.log(response)
        return response;
    }
    async function testFunc3(){
        const url = "https://localhost:9292/sub";
        await fetch(url, { mode: "no-cors" }).then((response) => console.log(response));
        return
    }
</script>

<h1>Post Issues</h1>

<button on:click={testFunc1}>testFunc1</button>
<button on:click={testFunc2}>testFunc2</button>
<button on:click={testFunc3}>testFunc3</button>