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
    background-image: url(./lib/scock3.jpg);
    background-repeat: none;
    background-size:cover;
    background-color:#fff;
    background-attachment: fixed;
    color:white;
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
  Lorem ipsum dolor sit amet consectetur adipisicing elit. Unde non, illum minima sit cupiditate doloribus architecto enim doloremque vero distinctio similique vitae itaque magnam facilis quod error adipisci, accusamus quos! Lorem ipsum dolor sit, amet consectetur adipisicing elit. Dolore, corporis officia laboriosam ipsa minus eligendi, quod provident distinctio, odit consequuntur deleniti voluptate magnam impedit aut animi odio? Aut, reiciendis expedita? Lorem ipsum dolor sit, amet consectetur adipisicing elit. Delectus cumque nobis numquam iusto mollitia sed dolorum, id ratione perferendis assumenda pariatur rerum sint corporis architecto incidunt laboriosam. Earum, provident corporis? Lorem ipsum dolor sit amet consectetur adipisicing elit. Mollitia consectetur recusandae voluptas veritatis natus numquam itaque, ipsa ad accusamus rerum commodi explicabo! Itaque similique incidunt vitae, commodi nam dolorem nostrum. Lorem ipsum dolor sit, amet consectetur adipisicing elit. Dolorum debitis hic odio at provident ea corrupti excepturi eveniet aspernatur. Incidunt laborum pariatur doloribus beatae sunt, quia id rerum perferendis molestiae? Lorem ipsum dolor sit amet consectetur adipisicing elit. Tenetur, doloribus perspiciatis quod laudantium ipsa cum numquam provident dolorem nam maiores illo. Veritatis impedit, veniam molestias necessitatibus tenetur cumque! Culpa, quidem.<br/><br/>
</maintwoelectricbogaloo>