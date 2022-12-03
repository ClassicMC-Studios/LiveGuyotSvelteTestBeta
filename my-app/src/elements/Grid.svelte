<script>
	import { text } from 'svelte/internal';
	import { fade, draw, fly } from 'svelte/transition';
	let visable = false;
	function startUp(){
		visable = true; 
	} 
</script>
<style>
	.item{
		background-color: #0d161d;
		text-align:center;
	}
/* 	.bleux{transition: 0.3s;}
	.bleux:hover{color: skyblue;} */
	blue{color:blue;}
	.hv{
		background-color: #0d161d;
		transition: 0.3s; 
	}
	.hv:hover{background-color: #182835;} 
	a{text-decoration: none;}
	a:hover{text-decoration: underline;}
	.shadow{
		text-shadow: 0px 0px 20px rgb(255, 255, 255);
	}
</style>
<svelte:window on:load={startUp()}/>
<main>
<!-- Layer 1	 -->
<div class="w3-row">
<!-- Item 1 -->
	<div class="w3-col item w3-margin bc-r-25 hv bc-border bc-bdc-white" style="width:220px; height:220px;">
		<p>
			Welcome to<br/><em>
				{#if visable}
					{#each 'Guyot' as text,i}
						<span in:fade="{{delay: 0 + i * 150, duration: 800}}">{text}</span>
					{/each}
				{/if}
			</em><br/>Keeping Chromebooks<br/><b>Open Source</b><br/>
			<img src="https://classicmc-studios.github.io/guyot/comp.png" alt="computer"/>
		</p>
	</div>
<!-- Item 2 -->
	<div class="item w3-col w3-margin bc-r-25 hv bc-border bc-bdc-white" style="width:220px; height:220px;">
		<p>We need</p>
		<h1><b>
			{#if visable}
				{#each 'Your Help' as text,i}
					<span class="shadow" in:fade="{{delay: 0 + i * 150, duration: 800}}">{text}</span>
				{/each}
			{/if}
		</b></h1>
		<p>To keep this site running</p>
		<h4>See <a href="https://guyotjs.github.io/east"><blue>positions</blue></a></h4>
	</div>
</div>
<!-- Layer 2 -->
<div class="w3-row">
<!-- Item 1	 -->
	<div class="w3-col item w3-margin bc-r-25 hv bc-border bc-bdc-white" style="width:220px; height:220px;">
		<h1><b>
			{#if visable}
				{#each 'v0.8.1' as text,i}
					<span class="shadow" in:fade="{{delay: 0 + i * 150, duration: 800}}">{text}</span>
				{/each}
			{/if}
		</b></h1>
		<p>
			<b>Changelog</b>
		</p>
		<p>
			- CSS now built in<br/>
			- White border added<br/>
			- New icons and shadow<br/>
			- Fade in effect
		</p>
	</div>
<!-- Item 2	 -->
	<div class="w3-col item w3-margin bc-r-25 hv bc-border bc-bdc-white" style="width:220px; height:220px;">
		<h1><b>
			{#if visable}
				{#each 'Info' as text,i}
					<span class="shadow" in:fade="{{delay: 0 + i * 150, duration: 800}}">{text}</span>
				{/each}
			{/if}
		</b></h1><p>
			This Website is changing!<br/>
			Visit the<br/>
			<b>
				<a href="https://guyotjs.github.io/beta"><h3>--Beta--</h3></a>
			</b>
	</div>
<!-- Upcoming -->
	<div class="w3-col item w3-margin bc-r-25 hv bc-border bc-bdc-white" style="width:220px; height:220px;">
		<h1>
			{#if visable}
				{#each 'Upcoming' as text,i}
					<span class="shadow" in:fade="{{delay: 0 + i * 150, duration: 800}}">{text}</span>
				{/each}
			{/if}
		</h1>
		<p><blue>Super Mario Kart(2ply*)</blue></p>
		<p><blue>Final Fantasy VI</blue></p>
		<p><blue>Pokémon Red</blue></p>
	</div>
</div>
</main>