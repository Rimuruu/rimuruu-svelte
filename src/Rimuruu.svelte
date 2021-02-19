<script>
  import Aside from "src/components/Aside.svelte";
  import Main from "src/components/Main.svelte";
  import { fly } from "svelte/transition";
  import { tweened } from 'svelte/motion';
  import AnimatedBG from 'src/components/AnimatedBG.svelte';

</script>

<style>
.row-reverse {display: flex; flex-direction: row-reverse; }
@media screen and (max-width: 830px) {
      .w-90 {
         display:none !important
      }
   }

</style>

<div class="container-fluid d-flex p-0 h-100 w-100 mw-100 min-vh-100">
<Aside></Aside>
<div class="container-fluid w-90 row-reverse mw-100 w-100 p-0">
<Main></Main>
</div>
</div>

  <AnimatedBG></AnimatedBG>
  