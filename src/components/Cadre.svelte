<script>
import Loadable from "svelte-loadable";
export let title;
export let info;
export let description;
export let link;
export let background;
let isOpen=false;



</script>
<style>

.modal-c {
  position: fixed; /* Stay in place */
  z-index: 1; /* Sit on top */
  left: 0;
  top: 0;
  width: 100%; /* Full width */
  height: 100%; /* Full height */
  overflow: auto; /* Enable scroll if needed */
  background-color: rgb(0,0,0); /* Fallback color */
  background-color: rgba(0,0,0,0.4); /* Black w/ opacity */
}
.modal-content-c {
  background-color: #fefefe;
  margin: 5px auto; /* 15% from the top and centered */
  padding: 20px;
  border: 1px solid #888;
  width: 50%; /* Could be more or less, depending on screen size */

}
.play,.play:focus,.play:active{
    background-color: transparent;
    border:none;
    outline: none;
  }

</style>
<div class="text-center border rounded p-5">
<h2>{title}</h2>
<p class="text-light">{info}<br>{description}</p>
{#if link !="tetris"}
<a href={link}><img 
    src="img/link.svg" 
    alt="link"
    height="50px"
    width="50px" /></a>
{:else}
<button class="play" on:click={()=>{isOpen = !isOpen}}>
<img 
    src="img/play-button.svg" 
    alt="link"
    height="50px"
    width="50px" />
</button>
{/if}
</div>

{#if isOpen}




<!-- Modal -->
<div class="modal-c">

<div class="modal-content-c">
<button on:click={()=>{isOpen = !isOpen}} class="bg-danger float-right"> X </button>
 <Loadable loader={() => import('src/game/Tetris.svelte')}>
    <div slot="loading">
      <div class="bg-dark bg-not-load text-center align-middle spin"><div class="spinner-border text-light " role="status">
  <span class="sr-only">Loading...</span>
</div></div>
    </div>
  </Loadable>
</div>
</div>



{/if}