<script>

let window;


</script>

<style>

.aside{
   -webkit-box-shadow: 9px -2px 6px -4px rgba(0,0,0,0.75);
-moz-box-shadow: 9px -2px 6px -4px rgba(0,0,0,0.75);
box-shadow: 9px -2px 6px -4px rgba(0,0,0,0.75);
}

@media screen and (min-width: 830px) {
      .aside {
         background-color: rgb(27, 27, 27);
         width:500px;
      }
   }

@media screen and (max-width: 830px) {
      .aside {
     
         width:100%;
      }
   }

.pic{
   -webkit-box-shadow: 6px 4px 23px 0px rgba(0,0,0,0.75);
-moz-box-shadow: 6px 4px 23px 0px rgba(0,0,0,0.75);
box-shadow: 6px 4px 23px 0px rgba(0,0,0,0.75);
   border-radius: 50%;
   width: 50%;
   margin-top:50%;
    margin-left: auto;
  margin-right: auto;
  display: block;
}
.text{
   margin-left: auto;
   margin-right: auto;
   display: block;
}
/*
 *  STYLE 1
 */

#style-1::-webkit-scrollbar-track
{
	-webkit-box-shadow: inset 0 0 6px rgba(0,0,0,0.3);
	border-radius: 10px;
	background-color: #F5F5F5;
}

#style-1::-webkit-scrollbar
{
	width: 12px;
	background-color: #F5F5F5;
}

#style-1::-webkit-scrollbar-thumb
{
	border-radius: 10px;
	-webkit-box-shadow: inset 0 0 6px rgba(0,0,0,.3);
	background-color: #555;
}


.margin-auto{
   margin-left: 30%;

}
.logo {
  vertical-align:top;
}
</style>
<svelte:window bind:innerWidth={window}/>

<div id="style-1" class="container-fluid aside h-100 min-vh-100 rounded-right m-0 text-light overflow-auto" >

<img class="pic" src="/img/pic.png" alt="pic">
<h2 class="text-center mt-5">Antoine Renciot</h2>
<div class="container my-3">
<div class="d-flex flex-column text ">
<a href="https://github.com/Rimuruu" class="margin-auto text-secondary"><img 
   class="mr-2 mt-1 logo"
    src="img/git.svg" 
    alt="github"
    height="20px"
    width="20px" />@rimuruu</a>
<a href="https://steamcommunity.com/id/MekakushiDainana/" class="margin-auto text-secondary"><img 
   class="mr-2 mt-1 logo"
    src="img/steam.svg" 
    alt="steam"
    height="20px"
    width="20px" />Ketto</a>
<a href="https://osu.ppy.sh/users/3186421" class="margin-auto text-secondary"><img 
   class="mr-2 mt-1 logo"
    src="img/osu.svg" 
    alt="osu"
    height="20px"
    width="20px" />Ketto</a>
<a href="https://myanimelist.net/animelist/ketto_sy" class="margin-auto text-secondary"><img 
   class="mr-2 mt-1 logo"
    src="img/mal.png" 
    alt="mal"
   height="20px"
    width="20px"
   /><span>ketto_sy</span></a>

</div>

</div>
<div class="d-flex flex-column text text-center">
<a href="mailto:antoine.renciot@gmail.com" class="text-muted my-5 text-italic"><img 
   class="mr-1 mt-1 logo"
    src="img/mail.svg" 
    alt="un triangle aux trois côtés égaux"
    height="20px"
    width="20px" />antoine.renciot@gmail.com</a>
</div>
</div>

