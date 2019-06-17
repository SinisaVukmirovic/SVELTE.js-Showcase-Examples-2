<script>
    let firstValue = 2;
    let secondValue = 7;
</script>

<label>
    <input type="number" bind:value={firstValue} min=0 max=10>
    <input type="range" bind:value={firstValue} min=0 max=10>
</label>

<label>
    <input type="number" bind:value={secondValue} min=0 max=10>
    <input type="range" bind:value={secondValue} min=0 max=10>
</label>

<p>Sum of ranges is: <strong>{firstValue} + {secondValue} = {firstValue + secondValue}</strong></p>