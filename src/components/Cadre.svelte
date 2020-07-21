<script>
export let title;
export let info;
export let description;
export let link;
export let background;




</script>
<div class="text-center border rounded p-5">
<h2>{title}</h2>
<p class="text-light">{info}<br>{description}</p>
<a href={link}><img 
    src="img/link.svg" 
    alt="link"
    height="50px"
    width="50px" /></a>

</div>