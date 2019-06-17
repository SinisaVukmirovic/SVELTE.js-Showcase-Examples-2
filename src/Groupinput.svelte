<script>
    let scoops = 1;
    let flavours = ['Mint choc chip'];

    let menu = [
        'Vanilla',
        'Mint choc chip',
        'Strawberry'
    ];

    const join = (flavours) => {
        if (flavours.length === 1) return flavours[0];

        return `${flavours.slice(0, -1).join(', ')} and ${flavours[flavours.length - 1]}`;
    }
</script>

<style>
    p {
        color: cornflowerblue;
    }
</style>

<h4>Icecream Portion</h4>

<label>
    <input type="radio" bind:group={scoops} value={1}>One Scoop
</label>

<label>
    <input type="radio" bind:group={scoops} value={2}>Two Scoops
</label>

<label>
    <input type="radio" bind:group={scoops} value={3}>Three Scoops
</label>

<h4>Icecream Flavours</h4>

{#each menu as flavour}
    <label>
        <input type="checkbox" bind:group={flavours} value={flavour}>{flavour}
    </label>
{/each}

{#if flavours.length === 0}
    <p>Please, select at least one flavour</p>
{:else if flavours.length > scoops}
    <p>Can't order more flavours that scoops</p>
{:else}
    <p>Your ordered {scoops} {scoops === 1 ? 'scoop' : 'scoops'} of {join(flavours)} icecream!</p>
{/if}