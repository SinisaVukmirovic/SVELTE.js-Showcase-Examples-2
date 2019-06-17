<script>
    let todos = [
        {
            done: false,
            text: 'Finish Svelte Tutorial'
        },
        {
            done: false,
            text: 'Build an App'
        },
        {
            done: false,
            text: 'Dominate the World'
        },
    ];

    $: remaining = todos.filter(todo => !todo.done).length;

    const addNew = () => {
        todos = todos.concat( { done: false, text: '' } );
    }
    const clearCompleted = () => {
        todos = todos.filter(todo => !todo.done);
    }
</script>

<style>
    .done {
        opacity: .4;
    }
</style>

{#each todos as todo}
    <div class:done={todo.done}>
        <input type=checkbox bind:checked={todo.done}>
        <input placeholder='What needs to be done?' bind:value={todo.text}>
    </div>
{/each}

<p>{remaining} remaining</p>

<button on:click={addNew}>Add New</button>
<button on:click={clearCompleted}>Clear Complited</button>