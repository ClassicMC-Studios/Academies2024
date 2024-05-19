<script>
  import Modal,{getModal} from './Modal2.svelte'
  let dark  ;
  export let butt;
	let selection
	function setSelection(res){
		selection=res
	}
</script>
<!-- <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/4.7.0/css/font-awesome.min.css"> -->
<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/4.7.0/css/font-awesome.min.css">
<style>.white{color:rgb(255, 255, 255)!important;}.bleu{color:rgb(108, 108, 239);}button{
  background-color: hsla(0, 0%, 27%, 0);
  border-radius: 0;
  color:white;
  border-color: black;
  border:1px solid white;
  padding:10px;
  /* transition: 0.3s; */
  font-size:20px;
  margin:10px;
}
input{
  background-color: rgba(0,0,0,0);
  border: 1px solid white;
  padding:5px;
  color:white;
}
button:hover{
  /* padding:20px; */
}</style>
<button class:white={dark}  on:click={()=>getModal().open()}>
  {butt}
</button>
<Modal>
  <em>
    <input type="text" placeholder="Speak here"> <button><i class="fa fa-send"></i></button>
  </em>
</Modal>