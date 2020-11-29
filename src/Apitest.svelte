<script>
    import CarbonBtn from "./CarbonBtn.svelte";
    let data = "not clicked";
    // let promise = getApiData();
    async function getApiData() {
        const res = await fetch(
            "http://www.7timer.info/bin/api.pl?lon=127&lat=37.5&product=astro&output=json"
        );
        const json = await res.json();
        if (res.ok) {
            data = JSON.stringify(json);
            return JSON.stringify(json);
        } else {
            throw new Error(json);
        }
    }
    // async function Api_test() {
    //     // promise = await getApiData();
    //     data = await getApiData();
    // }
</script>

<div>{data}</div>
<CarbonBtn handleClick={getApiData} name="Api Test">ApiTest</CarbonBtn>
<!-- {#await promise}
    <p>...waiting</p>
{:then jsonstr}
    <p>{jsonstr}</p>
{:catch error}
    <p>{error.message}</p>
{/await} -->
