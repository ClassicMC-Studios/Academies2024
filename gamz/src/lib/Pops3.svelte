<script>
  import Modal,{getModal} from './Modal3.svelte'
  let dark  ;
  export let butt;
	let selection
	function setSelection(res){
		selection=res
    }
</script>

<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/4.7.0/css/font-awesome.min.css">
<style>.white{color:rgb(255, 255, 255)!important;}.bleu{color:rgb(108, 108, 239);}button{
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
}</style>
<link rel="stylesheet" href="https://pyscript.net/releases/2024.5.2/core.css">
<!-- This script tag bootstraps PyScript -->
<svelte:head>
  <script type="module" src="https://pyscript.net/releases/2024.5.2/core.js"></script>
  <script src="http://code.jquery.com/jquery-3.3.1.min.js" integrity="sha256-FgpCb/KJQlLNfOu91ta32o/NMZxltwRo8QtmkMRdAu8=" crossorigin="anonymous"></script>
</svelte:head>
<button class:white={dark}  on:click={()=>getModal().open()}>
  {butt}
</button>
<Modal>
    Was he the killer? <input type="checkbox" name="" id=""><br/>
    Was his first victim a mom? <input type="checkbox" name="" id=""><br/>
    Were his victims stabbed? <input type="checkbox" name="" id=""><br/>
    Was he framed? <input type="checkbox" name="" id=""><br/>
</Modal>