<script>
	import { createEventDispatcher } from 'svelte';

	const dispatch = createEventDispatcher();
</script>

<style>
  	.modal-background {
		position: fixed;
		top: 0;
		left: 0;
		width: 100%;
		height: 100%;
		background: rgba(0,0,0,0.7);
  }
  
	.modal {
		position: absolute;
		left: 50%;
		top: 50%;
		width: 100vw;
		height: 50vh;
		overflow: auto;
		transform: translate(-50%,-50%);
		background: transparent;
	}
</style>

<div class='modal-background' on:click='{() => dispatch("close")}'></div>

<div class='modal' on:click='{() => dispatch("close")}'>
<!-- any children of modal compenent are rendered in slot. multiple slots can be used with ids -->
	<slot></slot> 
</div>
