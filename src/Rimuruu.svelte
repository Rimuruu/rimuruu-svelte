<script>
  import Aside from "src/components/Aside.svelte";
  import Main from "src/components/Main.svelte";
  import { fly } from "svelte/transition";
  import { tweened } from 'svelte/motion';
   import Loadable from "svelte-loadable";

</script>

<style>
.row-reverse {display: flex; flex-direction: row-reverse; }
@media screen and (max-width: 830px) {
      .w-90 {
         display:none !important
      }
   }
.bg-not-load{
     position: fixed;
  right: 0;
  bottom: 0;
  min-width: 100%;
  min-height: 100%;
  z-index: -2;
}
.spin{
  display: flex;
   align-items: center; 
   justify-content: center;
}
</style>

<div class="container-fluid d-flex p-0 h-100 w-100 mw-100 min-vh-100">
<Aside></Aside>
<div class="container-fluid w-90 row-reverse mw-100 w-100 p-0">
<Main></Main>
</div>
</div>
 
  
  <Loadable loader={() => import('src/components/AnimatedBG.svelte')}>
    <div slot="loading">
      <div class="bg-dark bg-not-load text-center align-middle spin"><div class="spinner-border text-light " role="status">
  <span class="sr-only">Loading...</span>
</div></div>
    </div>
  </Loadable>