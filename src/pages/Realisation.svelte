<script>
import Cadre from "src/components/Cadre.svelte"
import Real from "src/data/real.json"
console.log(Real);
</script>
<style>
.grid-r{
    display:grid;
   grid-template-columns: 1fr 1fr 1fr;

}
</style>
<div class="grid-r">
{#each Object.entries(Real) as [cle, valeur]}
<Cadre title={valeur.title} link={valeur.link} info={valeur.info} description={valeur.description} background={valeur.background}></Cadre>
{/each}

</div>