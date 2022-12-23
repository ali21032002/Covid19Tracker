<script context="module">
    export async function preload(page){
        console.log(page);
        return {state: page.params['state']};
    }
</script>

<script>
    export let state;
    import CovidStat from "../components/CovidStat.svelte";
    import CovidChart from "../components/CovidChart.svelte"; 
    import TableContainer from "../components/TableContainer.svelte";
</script>

<h1>{state}</h1>

<CovidStat/>
<CovidChart/>