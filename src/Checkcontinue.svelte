<script>
    let checked = false;
</script>

<style>
    button {
        margin: 0;
    }
</style>

<label>
    <input type="checkbox" bind:checked={checked}>
    Yes, I want to learn more about SVELTE.js!
</label>

{#if checked}
    <h6><em>Thank You! More about Svelte.js coming right up! Stay tuned! Lorem ipsum dolor sit amet consectetur adipisicing elit dolor consectetur adipisicing sit amet.</em></h6>
{:else}
    <h6><em>Please check the checkbox if you want to continue and learn more abour Svelte.js! Lorem ipsum dolor sit amet dolor sit.<em></h6>
{/if}

<!-- <button
    onclick="window.location.href = 'https://svelte.dev/';"
    disabled={!checked}>Continue</button> -->

<a href="https://svelte.dev/" target="_blank">
    <button disabled={!checked}>Continue</button>
</a>