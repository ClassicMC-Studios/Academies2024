<style>
  :global(body){
    background-image: url(./lib/scock3.jpg);
    background-repeat: none;
    background-size:cover;
    background-color:#fff;
    background-attachment: fixed;
    color:white;
  }
  button{
    background-color: hsla(0, 0%, 27%, 0);
    border-radius: 0;
    color:white;
    border-color: black;
    border:1px solid white;
    padding:10px;
    transition: 0.3s;
    font-size:20px;
    margin:10px;
  }
  button:hover{
    padding:20px;
  }
</style>
<script>
  import Pops from "./lib/Pops.svelte";
  import Pops2 from "./lib/Pops2.svelte";
  import Pops3 from "./lib/Pops3.svelte";
  import Pops4 from "./lib/Pops4.svelte";
  function random(min, max) {
    return Math.trunc(Math.random() * (max - min) + min)
  }
  let lang = random(0,4);
  /* 
    0: Tagalog
    1: Catalan
    2: Hindi
    3: Finnish
  */
</script>
<main>
  <h1>The Confession of a <em>Killer</em></h1>
  <Pops butt="View the Confession"/><Pops2 butt="Speak to Someone"/><br/>
  <Pops3 butt="Final Translation"/><Pops4 butt="Journal and Clues"/>
  
</main>