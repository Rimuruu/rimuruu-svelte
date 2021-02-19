
<script>
import {fade} from "svelte/transition"
import History from "src/pages/History.svelte"
import Realisation from "src/pages/Realisation.svelte"
import { onMount } from "svelte";
let main;
let container;
let isOpen = false;
let category="history";
let h,r;
function change(){
    category="history";
    if(isOpen){
        main.style.width = "0px";
        isOpen =false;
        
        }
    else{ 
        console.log((container-450) + "px")
        main.style.width = (container-450) + "px";
        isOpen =true;
        }
}

function changeH(){
            category="history";
            r.classList.remove("active");
            h.classList.add("active");
  
      
 
}

function changeR(){

            category="real";
            h.classList.remove("active");
            r.classList.add("active");
    
}

onMount(() => {
    change();
    
    });

</script>

<style>

.w-90{
     
    -webkit-box-shadow: -12px 1px 6px -4px rgba(0,0,0,0.75);
    -moz-box-shadow: -12px 1px 6px -4px rgba(0,0,0,0.75);
    box-shadow: -12px 1px 6px -4px rgba(0,0,0,0.75);
}

.article{
    width:0px;
    transition: width 1s;
     transition-timing-function: ease-in-out;
}
@media screen and (max-width: 830px) {
      .w-90 {
         display:none !important
      }
   }

   button:active{
    background-color: rgb(27, 27, 27);
}
 .open,.open:focus{
    outline:none;
    border: none;
}
.group-b *{
    background-color: transparent !important;

}
.group-b *:hover{
    background-color: 	#E6E6FA !important; 
    color:rgb(27, 27, 27) !important;
}
.active{
    background-color: 	#E6E6FA !important; 
    color:rgb(27, 27, 27) !important;
}
</style>

<svelte:window bind:innerWidth={container}/>
<div  class="rounded-left p-0 rounded-lg bg-very-dark main h-100 min-vh-100 text-light w-90 d-flex flex-row">

<button class="bg-very-dark open" on:click={change}><img 
   class="logo "
    src="img/menu.svg" 
    alt="un triangle aux trois côtés égaux"
   height="20px"
    width="20px"
   /></button>

<div bind:this={main} class=" article d-flex flex-column" >
{#if isOpen}
<div class="d-flex flex-column overflow-hidden" in:fade="{{ y: 200, duration: 1000,delay:500 }}">
<div   class="p-1 btn-group w-100 group-b" role="group" aria-label="Basic example">
  <button type="button" on:click={changeH} bind:this={h} class="btn btn-secondary active">History Log</button>
  <button type="button" on:click={changeR} bind:this={r} class="btn btn-secondary">Realisation</button>
</div>
<div class="container-fluid overflow-auto p-5">
{#if category == "history"}
<History/>
{:else if category == "real"}
<Realisation/>
{/if}
</div>
</div>
{/if}
</div>
</div>