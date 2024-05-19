<script>
  import Modal,{getModal} from './Modal4.svelte'
  let dark  ;
  export let butt;
	let selection
	function setSelection(res){
		selection=res
	}
  import fin from '../jsons/newfinnish.json'
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
<button class:white={dark}  on:click={()=>getModal().open()}>
  {butt}
</button>
<Modal>
  <em>
    <textarea name="" id="" style="background-color:rgba(0,0,0,0); width:500px;height:300px; color:white;" placeholder="Type your notes here"></textarea>
  <br/>  I was asleep at night is : {fin.i} {fin.was} {fin.asleep} {fin.at} {fin.night}<br/>
Does your dad like me is : {fin.does} {fin.your} {fin.dad} {fin.like} {fin.me}<br/>
The family does not believe me is: {fin.the} {fin.family} {fin.does} {fin.not} {fin.believe} {fin.me} 
  </em>
</Modal>