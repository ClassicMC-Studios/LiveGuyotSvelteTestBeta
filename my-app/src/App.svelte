<script>
	import Sidebar from './elements/Sidebar.svelte';
	import Grid from './elements/Grid.svelte';
	import Appbar from './elements/Appbar.svelte';
	import Newsbar from './elements/Newsbar.svelte';
	import Sno from './Sno.svelte';
</script>
<link href="https://fonts.googleapis.com/icon?family=Material+Icons" rel="stylesheet">
<style>
	:global(body){
		margin: 0%;
		padding: 0%;
		/* A whole bunch of garbage to get backgrounds working */
		background-image: url("./assets/christmas-ducky.png");
		background-repeat:no-repeat;
		background-size: cover;
		background-position: center center;
		background-attachment: fixed;
		color: #bfc2c7;
		font-family: sans-serif;
	}
	.content{
		margin: 0%;
    	margin-left: 80px;
	}
</style>
<main>
	<Sidebar/>
	<div class="content"> 
		<Grid/>
		<Appbar/>
		<Newsbar/>
	</div>
	<Sno/>
</main>