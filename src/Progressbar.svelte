<script>
    import { tweened } from 'svelte/motion';
    import { cubicOut } from 'svelte/easing';

    const progress = tweened (.25, {
        duration: 400,
        easing: cubicOut
    });
</script>

<style>
    progress {
        display: block;
        width: 100%;
        margin-bottom: 1em;
    }
    button {
        margin-right: .5em;
    }
</style>

<progress value={$progress}></progress>

<button on:click={() => progress.set(0)}>0%</button>
<button on:click={() => progress.set(.25)}>25%</button>
<button on:click={() => progress.set(.50)}>50%</button>
<button on:click={() => progress.set(.75)}>75%</button>
<button on:click={() => progress.set(1)}>100%</button>