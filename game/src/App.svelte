<script>
  import { fade } from 'svelte/transition';
  import Txt from './lib/txt.svelte'
  import Roll from './lib/roll.svelte'
  let visable = false;
  function startUp(){visable = true;}
</script>
<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/4.7.0/css/font-awesome.min.css">
<style>
  :global(body){
    background-image: url(./lib/skibidi.jpg);
    background-repeat: none;
    background-size:cover;
    background-attachment: fixed;
  }
</style>
<svelte:window
  on:load={startUp()}
/>
<main>
  {#each 'decoder' as letter, i}
    {#if visable}
      <span class="h1" in:fade={{delay: 100 + i * 150, duration: 800}}>{letter}</span>
    {/if}
  {/each}<br/>
  <Txt txt='In axit orem des livi'/><br/><br/><br/><br/>
  
  {#if visable}
    <div in:fade={{delay: 2510 + 2 * 150, duration: 800}}>    
      <Roll/>
    </div>
  {/if}
</main>
<maintwoelectricbogaloo>
  skibidi
</maintwoelectricbogaloo>