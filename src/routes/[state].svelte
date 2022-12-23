<script context="module">
    import PageTitle from "../components/PageTitle.svelte"; 
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

<PageTitle pageName={state}/>

<div class="section header">
    <div class="container">
        <h1>Covid 19 - {state}</h1>
    </div>
</div>



<CovidStat/>
<CovidChart/>