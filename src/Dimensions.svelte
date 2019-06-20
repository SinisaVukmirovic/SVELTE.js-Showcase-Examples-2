<script>
    let w;
    let h;
    let size = 30;
</script>

<style>
    p {
        color: cornflowerblue;
    }
	input { 
        display: block; 
        margin-bottom: 1em; 
    }
	div {
        display: inline-block;
        overflow: hidden;
        max-width: 100%;
    }
</style>

<p>Current Logo Size: {w}px &times; {h}px</p>

<input type="range" bind:value={size} min="10" max="100">

<div bind:clientWidth={w} bind:clientHeight={h}>
	<img style="height: {size * 2}px;" src="./img/svelte-logo-horizontal.svg" alt="Svelte Logo">
</div>




