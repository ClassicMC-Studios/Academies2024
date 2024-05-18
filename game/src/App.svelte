<script>
  import { fade } from 'svelte/transition';
  let visable = false;
  function startUp(){visable = true;}
</script>
<style>

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
  {#each 'In axit avim des orem' as letter,i}
     {#if visable}
      <span class="em" in:fade={{delay: 2000 + i * 50, duration: 0}}>{letter}</span>
     {/if}
  {/each}
</main>